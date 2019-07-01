<template>
    <div class="products">
        <h1 class="subheading grey--text">معرفی بعضی از محصولات</h1>

        <v-container class="pa-4 mt-3" grid-list-md>
            <v-layout row wrap>
                <v-flex xs12 md6 lg4 v-for="i in 5" :key="i">
                    <!-- 
                    <v-expansion-panel>
                        <v-expansion-panel-content v-for="project in projects" :key="project.title">
                        <div slot="header">{{project.title}}</div>
                        <v-card>
                            <v-card-text class="grey--text px-4">
                            <div class="font-weight-bold">{{project.due}}</div>
                            <div>{{project.content}}</div>
                            </v-card-text>
                        </v-card>
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                    -->
                    <v-card dark class="grey darken-3 px-1 py-2">
                        <v-layout row>
                            <v-flex xs5 sm6 md6>
                                <v-card-title primary-title>
                                    <div>
                                        <div class="headline">T-53</div>
                                        <div class="mt-3">ساخت ایران</div>
                                    </div>
                                </v-card-title>
                            </v-flex>
                            <v-flex xs7 sm6 md6>
                                <v-img
                                src="https://www.compass-italy.com/pimages/Beeper-extra-big-65-707.png"
                                height="200px"
                                contain
                                ></v-img>
                            </v-flex>
                        </v-layout>
                        <!-- read more -->
                        <v-divider class="yellow"></v-divider>
                        <v-expansion-panel class="grey" focusable>
                            <v-expansion-panel-content>
                                <div slot="header">Read More</div>
                                <v-card>
                                    <v-card-text class="white--text px-4">
                                        <div>
                                            این محصول ساخته شده از بهترین مواد و وسال ممکن توسط متخصصان داخلی
                                            است که ةرفیت صادرات و برد 4000 متری را داراست.
                                        </div>
                                    </v-card-text>
                                </v-card>
                            </v-expansion-panel-content>
                        </v-expansion-panel>

                        <v-divider class="yellow"></v-divider>
                        <v-card-actions>
                            <div class="mt-2">قیمت : {{4000}}</div>
                            <v-spacer></v-spacer>
                            <v-btn color="success">
                                <v-icon>shopping_cart</v-icon>
                            </v-btn>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

</style>
