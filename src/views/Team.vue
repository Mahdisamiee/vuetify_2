<template>
    <main>
        <h1 class="text-xs-center teal--text">تیم ما</h1>
        <v-container grid-list-md>
            <v-layout row wrap>
                <v-flex xs12 sm6 md3>
                    <v-card flat class="text-xs-center">
                        <div class="pa-3">
                            <v-avatar
                                size="100"
                                color="teal"
                            >
                                <img src="https://www.seoclerk.com/pics/319222-1IvI0s1421931178.png" alt="alt">
                            </v-avatar>
                        </div>
                        <v-card-text>
                            <div class="subheading teal--text">Mr.samiee</div>
                            <div class="grey--text">Front-End developer</div>
                        </v-card-text>
                        <v-divider></v-divider>
                        <v-card-actions>
                            <v-layout column>
                                <v-flex xs12>
                                    <p>من رو در شبکه های اجتماعی دنبال کنید</p>
                                </v-flex>
                                <v-flex xs12>
                                    <div>
                                        <v-btn
                                            v-for="icon in icons"
                                            :key="icon"
                                            icon
                                            class="teal--text"
                                        >
                                        <v-icon size="24px">{{ icon }}</v-icon>
                                        </v-btn>
                                    </div>
                                </v-flex>
                            </v-layout>
                        </v-card-actions>
                    </v-card>
                </v-flex>
                <v-flex xs12 sm6 md3>
                    <v-card flat class="text-xs-center">
                        <div class="pa-3">
                            <v-avatar
                                size="100"
                                color="teal"
                            >
                                <img src="http://cliparts101.com/files/367/63BA654AECB7FD26A32D08915C923030/avatar_nick.png" alt="alt">
                            </v-avatar>
                        </div>
                        <v-card-text>
                            <div class="subheading teal--text">Mr.Moradi</div>
                            <div class="grey--text">Back-End developer</div>
                        </v-card-text>
                        <v-divider></v-divider>
                        <v-card-actions>
                            <v-layout column>
                                <v-flex xs12>
                                    <p>من رو در شبکه های اجتماعی دنبال کنید</p>
                                </v-flex>
                                <v-flex xs12>
                                    <div>
                                        <v-btn
                                            v-for="icon in icons"
                                            :key="icon"
                                            icon
                                            class="teal--text"
                                        >
                                        <v-icon size="24px">{{ icon }}</v-icon>
                                        </v-btn>
                                    </div>
                                </v-flex>
                            </v-layout>
                        </v-card-actions>
                    </v-card>
                </v-flex>
                <v-flex xs12 sm6 md3>
                    <v-card flat class="text-xs-center">
                        <div class="pa-3">
                            <v-avatar
                                size="100"
                                color="teal"
                            >
                                <img src="https://webiconspng.com/wp-content/uploads/2017/09/Mr.-Bean-PNG-Image-40792-300x300.png   " alt="alt">
                            </v-avatar>
                        </div>
                        <v-card-text>
                            <div class="subheading teal--text">Mr.Hoda</div>
                            <div class="grey--text">Django developer</div>
                        </v-card-text>
                        <v-divider></v-divider>
                        <v-card-actions>
                            <v-layout column>
                                <v-flex xs12>
                                    <p>من رو در شبکه های اجتماعی دنبال کنید</p>
                                </v-flex>
                                <v-flex xs12>
                                    <div>
                                        <v-btn
                                            v-for="icon in icons"
                                            :key="icon"
                                            icon
                                            class="teal--text"
                                        >
                                        <v-icon size="24px">{{ icon }}</v-icon>
                                        </v-btn>
                                    </div>
                                </v-flex>
                            </v-layout>
                        </v-card-actions>
                    </v-card>
                </v-flex>
                <v-flex xs12 sm6 md3>
                    <v-card flat class="text-xs-center">
                        <div class="pa-3">
                            <v-avatar
                                size="100"
                                color="teal"
                            >
                                <img src="https://fiverr-res.cloudinary.com/images/t_main1,q_auto,f_auto/gigs/1542095/original/2488f9307929fde6c5184f6343ecd4ac2a526f60/draw-avatar-of-you-from-photo.png" alt="alt">
                            </v-avatar>
                        </div>
                        <v-card-text>
                            <div class="subheading teal--text">Mr.Nafar</div>
                            <div class="grey--text">Android developer</div>
                        </v-card-text>
                        <v-divider></v-divider>
                        <v-card-actions>
                            <v-layout column>
                                <v-flex xs12>
                                    <p>من رو در شبکه های اجتماعی دنبال کنید</p>
                                </v-flex>
                                <v-flex xs12>
                                    <div>
                                        <v-btn
                                            v-for="icon in icons"
                                            :key="icon"
                                            icon
                                            class="teal--text"
                                        >
                                        <v-icon size="24px">{{ icon }}</v-icon>
                                        </v-btn>
                                    </div>
                                </v-flex>
                            </v-layout>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>
    </main>
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
