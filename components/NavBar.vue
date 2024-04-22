<template>
    <nav class="flex justify-between items-center shadow-md py-3 sticky top-0 z-10">
        <!-- LOGO -->
        <div class="ml-5 md:ml-10">
            <h1 class="text-green-500 text-4xl rounded-full text-center cursor-pointer py-1"
                style="width: 50px; height: 50px; border: 1px solid; border-radius: 50%;">M</h1>
        </div>
        <!-- LINKS IN LARGE SCREEN -->
        <div class="mr-10 hidden lg:block">
            <ul class="flex gap-20 items-center font-semibold">
                <li>HOME</li>
                <li>ABOUT</li>
                <li>SERVICES</li>
                <li>PORTFOLIO</li>
                <li class="flex gap-2 items-center">
                    <h1>Theme Mode:</h1><select v-model="$colorMode.preference" class="px-2 py-1 text-center"
                        style="border: 1px solid;">
                        <option value="system">System</option>
                        <option value="light">Light</option>
                        <option value="dark">Dark</option>
                        <option value="sepia">Sepia</option>
                    </select>
                </li>
            </ul>
        </div>
        <!-- LINKS IN SMALL SCREEN -->
        <div class="mr-5 md:mr-10 lg:hidden flex items-center gap-2" >
            <h1>Theme Mode:</h1><select v-model="$colorMode.preference" class="px-2 py-1 rounded text-center"
                style="border: 1px solid ;">
                <option value="system">System</option>
                <option value="light">Light</option>
                <option value="dark">Dark</option>
                <option value="sepia">Sepia</option>
            </select>
            <DropMenu />

        </div>
    </nav>
</template>

<script setup>
const colorMode = useColorMode()

</script>

<style>
body {
    background-color: #fff;
    color: rgba(0, 0, 0, 0.8);
}

body nav {
    background-color: #dbd5d5;
}
.dark-mode body {
    background-color: #091a28;
    color: #19c53e;
    border-color: #19c53e;
}
.dark-mode nav{
    background-color: #0e3250;

}
.sepia-mode body {
    background-color: #f1e7d0;
    color: #433422;
}
.sepia-mode nav{
    background-color: #f5dda8;

}
</style>