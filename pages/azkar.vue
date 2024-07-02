<template>
  <v-app>
    <v-main>
      <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100 dark:bg-gray-900 ">
        <div  class="py-12 px-8 max-w-md w-full text-center relative shadow-xl rounded bg-gray-100 dark:bg-slate-700">
          <h1 class="text-2xl font-bold mb-4 dark:text-white">سبحة الأذكار الإلكترونية</h1>
          <div class="flex justify-end mb-4">
            <v-icon @click="toggleDarkMode" class="cursor-pointer">
              {{ darkModeIcon }}
            </v-icon>
          </div>
          <v-select
            v-model="selectedDhikr"
            :items="dhikrOptions"
            label="اختر الذكر"
            class="mb-4 dark:text-white"
            @change="handleDhikrChange"
          ></v-select>
          
          <div class="mb-6">
            <div class="inset-0 flex items-center justify-center">
              <span class="bg-white dark:bg-gray-700 rounded-full border-4 border-gray-300 dark:border-gray-600 text-3xl font-bold p-4 shadow-lg mx-auto text-center">
                {{ count }}
              </span>
            </div>
          </div>
          <div class="flex justify-center gap-2"><v-btn color="secondary" @click="reset">إعادة التعيين</v-btn>
            <v-btn color="primary" @click="increment">تسبيح</v-btn></div>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script setup>
import { ref, watch, computed } from 'vue'
import 'vuetify/styles'
import { createVuetify } from 'vuetify'

const vuetify = createVuetify()

const count = ref(0)
const selectedDhikr = ref('')
const customDhikr = ref('')
const dhikrOptions = ref([
  'سبحان الله', 'الحمد لله', 'الله أكبر', 'لا إله إلا الله', 'لا حول ولا قوة إلا بالله', 
  'أستغفر الله', 'اللهم صل على سيدنا محمد', 'سبحان الله وبحمده سبحان الله العظيم'
])
const colorMode = useColorMode()

const darkModeIcon = computed(() => (colorMode.preference === 'dark' ? 'mdi-weather-sunny' : 'mdi-weather-night'))

// Computed property to determine card background color based on color mode
const cardClasses = computed(() => ({
  'dark:bg-gray-900': colorMode.preference === 'dark',
  'bg-gray-100': colorMode.preference !== 'dark',
}))

function increment() {
  count.value++
}

function reset() {
  count.value = 0
}

function handleDhikrChange() {
  reset()
}

function addCustomDhikr() {
  if (customDhikr.value && !dhikrOptions.value.includes(customDhikr.value)) {
    dhikrOptions.value.push(customDhikr.value)
    selectedDhikr.value = customDhikr.value
    customDhikr.value = ''
  }
  reset()
}

function toggleDarkMode() {
  colorMode.preference = colorMode.preference === 'dark' ? 'light' : 'dark'
}

watch(selectedDhikr, handleDhikrChange)
watch(customDhikr, addCustomDhikr)
</script>

<style scoped>
.relative {
  position: relative;
}
.absolute {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.cursor-pointer {
  cursor: pointer;
}
</style>
