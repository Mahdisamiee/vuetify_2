<template>
  <div class="home">
    <!-- toolbar -->
    <v-toolbar flat class="toolbar1 red mb-2">
      <v-layout row wrap  align-center>
        <v-flex  sm8>
          <v-layout row wrap>
            <v-flex xs4>
                <v-tooltip bottom>
                    <v-btn flat small color="white" slot="activator">
                        <v-icon >euro_symbol</v-icon>
                    </v-btn>
                    <span>مرتب سازی بر اساس قیمت</span>
                </v-tooltip>
            </v-flex>
              
            <v-flex xs4>
                <v-tooltip bottom>
                    <v-btn flat small color="white" slot="activator">
                        <v-icon >class</v-icon>
                    </v-btn>
                    <span>مرتب سازی بر اساس اسم</span>
                </v-tooltip>
            </v-flex>
              
            <v-flex xs4>
                <v-tooltip bottom>
                    <v-btn flat small color="white" slot="activator">
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
    <!-- container -->
    <v-card>
        <v-layout row wrap grid-list-lg class="py-3">
          <v-flex xs12 sm3 justify-center align-center class="px-3 mb-2" >
            <img max-width="100%" width="100%" height="450" src="https://dkstatics-public-2.digikala.com/digikala-adservice-banners/1000005662.jpg" alt="">
          </v-flex> 
          <v-flex  xs12 sm9 class="px-3 mb-2">
            <v-carousel height="450" interval="4000">
              <v-carousel-item
                v-for="(item ,i) in items"
                :key="i"
                :src="item.src"
              ></v-carousel-item>
            </v-carousel>
          </v-flex>
          <v-flex xs12 sm8 class="px-3 mb-2">
            <div class="teamdiv">
              <h2 class="white--text text-sm-center mt-4">ما یک تیم هستیم</h2>
              <v-layout row wrap>
                <v-flex xs12 sm6 md3>
                  <v-chip small class="primary white--text">
                    <v-icon left>supervisor_account</v-icon>همه با هم
                  </v-chip>
                </v-flex>
                <v-flex xs12 sm6 md3>
                  <v-chip small class="red lighten-1 white--text">
                    <v-icon left>accessibility_new</v-icon>برای پیشرفت
                  </v-chip>
                </v-flex>
                <v-flex xs12 sm6 md3>
                  <v-chip small class="teal white--text">
                    <v-icon left>stars</v-icon>بهترین محصول
                  </v-chip>
                </v-flex>
                <v-flex xs12 sm6 md3>
                  <v-chip small class="purple accent-4 white--text">
                    <v-icon left>build</v-icon>میسازیم
                  </v-chip>
                </v-flex>
              </v-layout>
            </div>
          </v-flex>
          <v-flex xs12 sm4 class="px-3 mb-2" >
            <v-card class="pt-5 pb-2">
              <v-card-title class="" primary-title>
                <img width="100%" max-width="100" src="https://www.communicaid.com/wp-content/uploads/2017/01/img-learnlight-11-cta-image-2.png" alt="">
              </v-card-title>
              <v-spacer></v-spacer>
              <v-card-actions class="mb-0">
                <v-tooltip bottom>
                  <v-btn class="mb-0" flat color="success" slot="activator">
                    <v-icon color="primary" right>dashboard</v-icon>
                    <span>
                      <router-link to="/products">مشاهده محصولات</router-link>
                    </span>
                  </v-btn>
                  <span>صفحه محصولات</span>
                </v-tooltip>
              </v-card-actions>
            </v-card>
          </v-flex>
      </v-layout>
      <div class="parallex-div ma-3">
        <div class="parallex-div-text">
            <span class="white--text">
                <h2>ما به فکر بهترین ها هستیم</h2>
            </span>
            <span class="white--text">
              <p class="pa-3">بهترین تولید کننده در ایران</p>
            </span>
        </div>
      </div>
      <v-layout row wrap grid-list-xl class="pa-3">
        <v-flex xs12 sm6 md4 v-for="i in 3" :key="i">
          <v-card class="cyan darken-2 white--text pa-3 ma-2">
            <v-layout column align-center class="pa-2 my-3">
              <v-avatar
                size="150"
                color="red"
              >
                <img src="https://cdn.vuetifyjs.com/images/cards/foster.jpg" alt="alt">
              </v-avatar>
            </v-layout>
            <v-divider></v-divider>
            <v-card-actions  class="pa-3">
              <div class="mx-auto" block>
                <v-rating
                  v-model="rate"
                  color="yellow darken-2"
                  hover
                ></v-rating>
              </div>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-card>
  </div>
</template>
<script>

  export default {
    data(){
      return{
        items: [
          {
            src: 'https://dkstatics-public.digikala.com/digikala-products/710659.jpg?x-oss-process=image/resize,h_800/quality,q_80'
          },
          {
            src: 'https://dkstatics-public.digikala.com/digikala-products/110681111.jpg?x-oss-process=image/resize,h_800/quality,q_80'
          },
          {
            src: 'https://dkstatics-public-2.digikala.com/digikala-products/110690701.jpg?x-oss-process=image/resize,h_800/quality,q_80'
          },
          {
            src: 'https://dkstatics-public.digikala.com/digikala-products/4710444.jpg?x-oss-process=image/resize,h_800/quality,q_80'
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .v-toolbar.toolbar1{
    border-radius: 2px;
  }
  .teamdiv{
    padding: 30px;
    background-image: url("https://images.pexels.com/photos/209640/pexels-photo-209640.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500") ;
    min-height: 500px;
    background-size: cover;
    display: grid;
    grid-template-rows: 2fr 1fr;
  }
  .teamdiv .layout{
    margin-top: 20px;
  }
  .v-btn__content a{
    text-decoration: none;
  }
  .parallex-div{
    position: relative;
    background-image: url("https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    min-height: 500px;
    background-attachment: fixed;
  }
  .parallex-div .parallex-div-text{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50% , -50%);
    font-size: 24px;
  }
  .v-input.v-text-field{
    background-color: white;
    height: 50px;
    padding: 5px;
    border-radius: 4px;
  }
</style>
