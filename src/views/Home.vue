<template>
  <div class="home">
    <v-card>
        <v-layout row wrap grid-list-lg class="py-3">
          <v-flex xs12 sm3 justify-center align-center class="px-3 mb-2" >
            <img max-width="100%" width="100%" height="400" src="https://dkstatics-public-2.digikala.com/digikala-adservice-banners/1000005662.jpg" alt="">
          </v-flex> 
          <v-flex xs12 sm9 class="px-3 mb-2">
            <v-carousel height="400" interval="4000">
              <v-carousel-item
                v-for="(item ,i) in items"
                :key="i"
                :src="item.src"
              ></v-carousel-item>
            </v-carousel>
          </v-flex>
          <v-flex xs12 sm8 height="400" class="px-3 mb-2">
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
                    <v-icon left>stars</v-icon>بهترین محصولات
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
          <v-flex xs12 sm4 class="px-3 mb-2">
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
                      <router-link to="/products">محصولات</router-link>
                    </span>
                  </v-btn>
                  <span>صفحه محصولات</span>
                </v-tooltip>
              </v-card-actions>
            </v-card>
          </v-flex>
      </v-layout>
      <div class="parallex">
        <h2>دنیایی از محصولات</h2>
      </div>
      <v-layout row wrap grid-list-xl>
        <v-flex xs12 sm6 md4>
          
        </v-flex>
        <v-flex xs12 sm6 md4>
          
        </v-flex>
        <v-flex xs12 sm6 md4>
          
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
  .teamdiv{
    padding: 30px;
    background-image: url("https://images.pexels.com/photos/209640/pexels-photo-209640.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500") ;
    min-height: 500px;
    background-size: cover;
    display: grid;
    grid-template-rows: 2fr 1fr;
  }
  .teamdiv .layout{
    
  }
  .v-btn__content a{
    text-decoration: none;
  }
</style>
