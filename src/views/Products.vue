<template>
    <div class="products">
        <v-toolbar flat class="toolbar1 white">
            <v-layout row wrap  align-center>
                <v-flex  sm8>
                    <v-layout row wrap>
                        <v-flex xs4>
                            <v-tooltip bottom>
                                <v-btn flat small color="grey" slot="activator">
                                    <v-icon >euro_symbol</v-icon>
                                </v-btn>
                                <span>مرتب سازی بر اساس قیمت</span>
                            </v-tooltip>
                        </v-flex>
                        
                        <v-flex xs4>
                            <v-tooltip bottom>
                                <v-btn flat small color="grey" slot="activator">
                                    <v-icon >class</v-icon>
                                </v-btn>
                                <span>مرتب سازی بر اساس اسم</span>
                            </v-tooltip>
                        </v-flex>
                        
                        <v-flex xs4>
                            <v-tooltip bottom>
                                <v-btn flat small color="grey" slot="activator">
                                    <v-icon >favorite</v-icon>
                                </v-btn>
                                <span>بیشترین علاقه</span>
                            </v-tooltip>
                        </v-flex>
                    </v-layout>
                </v-flex>
                <v-spacer></v-spacer>
                <v-flex hidden-xs-only  sm4>
                    <v-text-field prepend-icon="search" single-line></v-text-field>
                </v-flex>
            </v-layout>
        </v-toolbar>

        <v-container class="pa-4 mt-3" grid-list-lg>
            <v-layout row wrap>
                <v-flex xs12 md6 lg4 v-for="i in 5" :key="i">
                    <v-card dark class="product-box grey darken-3 px-1 py-3 ">
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
                        <v-expansion-panel class="grey" >
                            <v-expansion-panel-content class="text-xs-right">
                                <div slot="header" >مشخصات</div>
                                <v-card>
                                    <v-card-text right class="white--text px-4">
                                        <div >
                                            این محصول ساخته شده از بهترین مواد و وسائل ممکن توسط متخصصان داخلی
                                            است که ظرفیت صادرات و برد 4000 متری را داراست.
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
.v-toolbar.toolbar1{
    border-radius: 50px;
}
.product-box{
    border-radius: 10px;
}
</style>
