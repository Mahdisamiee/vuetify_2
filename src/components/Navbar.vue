<template>
    <nav>
        <v-toolbar flat dark  color="" app>
            <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-text class="white--text title  mr-4 text-truncate">
                <h1>
                    <span class="text-capitalize font-weight-light">new</span>
                    <span class="text-capitalize font-weight-medium">Site</span>
                </h1>
            </v-toolbar-text>
            <v-spacer></v-spacer>
            
            <v-btn class="white grey--text" flat small>
                <span>خروج</span>
                <v-icon small left>exit_to_app</v-icon>
            </v-btn>
            <Register/>
        </v-toolbar>
        <v-navigation-drawer right v-model="drawer" app dark class="lighten-2">
            <v-list>
                <v-list-tile dark v-for="item in items" :key="item.title" avatar router :to="item.route">
                    <v-list-tile-action>
                        <v-icon>{{item.icon}}</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content class="mr-3">
                        <v-list-tile-title class="white--text">
                            {{item.text}}
                        </v-list-tile-title>
                    </v-list-tile-content>

                    
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>
import Register from "./Register.vue"

export default {
    components:{
        Register,
    },
    data(){
        return{
            drawer: false, // for <v-navigation-drawer>
            items: [
                { icon:'home' , text:'صفحه اصلی' , route:'/'},
                { icon:'folder' , text:'محصولات' , route:'/products'},
                { icon:'person' , text:'تیم ما' , route:'/team'}
            ]
        }
    }
}
</script>

<style scoped>
.v-toolbar{
    border-bottom: 3px solid gold
}
.v-list__tile__action{
    color: gold;
}

</style>
