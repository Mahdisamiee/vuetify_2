<template>
    <v-footer
    dark
    height="auto"
    class="mt-3"
    >
        <v-card
        class="flex"
        flat
        tile
        >
        <v-card-title class="teal darken-3">
            <strong class="subheading  mx-4">ما را در شبکه های اجتماعی دنبال کنید</strong>

            <v-spacer></v-spacer>

            <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            dark
            icon
            >
            <v-icon size="24px">{{ icon }}</v-icon>
            </v-btn>
        </v-card-title>

        <v-card-actions class="grey darken-3 justify-center">
            &copy;2018 — <strong>Vuetify</strong>
        </v-card-actions>
        </v-card>
    </v-footer>
</template>

<script>
export default {
    data(){
        return{
            icons: [
                'fab fa-facebook',
                'fab fa-twitter',
                'fab fa-google-plus',
                'fab fa-linkedin',
                'fab fa-instagram'
            ]
        }
    }
}
</script>

