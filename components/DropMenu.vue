<template>
    <v-row>
        <v-col>
            <v-card-title>


                <v-menu>
                    <template v-slot:activator="{ props }">
                        <v-btn icon="mdi-menu" v-bind="props" color="green"></v-btn>
                    </template>

                    <v-list>
                        <v-list-item >
                            <v-list-item-title class="mb-3">HOME</v-list-item-title>
                            <v-list-item-title class="mb-3">ABOUT</v-list-item-title>
                            <v-list-item-title class="mb-3">SERVICES</v-list-item-title>
                            <v-list-item-title>PORTFOLIO</v-list-item-title>
                        </v-list-item>
                    </v-list>
                </v-menu>
            </v-card-title>


        </v-col>
    </v-row>
</template>
<script>
export default {
    data: () => ({
        items: [
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me 2' },
        ],
    }),
}
</script>