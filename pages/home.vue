<template>
  <v-responsive class="border rounded" max-height="auto">
      <v-app >
          <v-app-bar :elevation="2" color="grey-darken-4">
              <template v-slot:prepend>
                  <v-app-bar-nav-icon></v-app-bar-nav-icon>
              </template>

              <!-- <v-app-bar-title> email:{{ email }}  username={{ username }}</v-app-bar-title> -->
              <div class="text-center">
                  {{ email }}
                  <v-btn  prepend-icon="mdi-check-circle" @click="logout">
                      <template v-slot:prepend>
                          <v-icon color="success"></v-icon>
                      </template>
                      Logout
                  </v-btn>
              </div>
          </v-app-bar>

<v-carousel show-arrows="hover" hide-delimiters>
    <v-carousel-item>
      <v-img
        src="https://www.bigbike.in.th/images/upload/topics/8525/Kawasaki/kawasaki-ninja-h2-2024-2.jpeg"
        contain
        class="custom-carousel-item"
      ></v-img>
    </v-carousel-item>

    <v-carousel-item>
      <v-img
        src="https://www.webike.my/my_news/wp-content/uploads/2022/10/cp166_trick-star_ninja-h2_01.jpg"
        contain
        class="custom-carousel-item"
      ></v-img>
    </v-carousel-item>

    <v-carousel-item>
      <v-img
        src="https://soymotero.net/wp-content/uploads/2021/10/nueva_kawasaki_ninja_h2r_curva_circuito.jpg"
        contain
        class="custom-carousel-item"
      ></v-img>
    </v-carousel-item>
  </v-carousel>
  <v-row align="center" justify="center" dense>
                <v-col cols="12 pt-3" md="6">
                    <v-card elevation="16" append-avatar=" " class="mx-auto"
                     prepend-avatar="https://ae01.alicdn.com/kf/S9aa446850c25477d84d58051ab90c3ddY/Fairing.png"
                        subtitle="รถซุปเปอร์ไบค์ที่เเรงที่สุดในโลก" title="Kawasaki Ninja H2®">
                        <v-card-text>ทีเด็ดของมอเตอร์ไซค์ต้นแบบรุ่นนี้อยู่ที่เครื่องยนต์ 4 สูบ ขนาด 998 ซีซี ที่ติดตั้งซูเปอร์ชาร์จ ให้กำลัง 300 แรงม้า ตัวซุปเปอร์ชาร์จรับลมจากช่องลมด้านหน้า เพื่อเพิ่มกำลังของเครื่องยนต์ โดยคาวาซากิตั้งใจให้มันสามารถทำความเร็วถึง 320 กม./ชม. ได้แบบสบาย ๆ
                        </v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12 pt-3" md="6">
                    <v-card elevation="16" class="mx-auto" subtitle="prepend and append" title="Icons">
                        <template v-slot:prepend>
                            <v-icon color="primary" icon="mdi-account"></v-icon>
                        </template>
                        <template v-slot:append>
                            <v-icon color="success" icon="mdi-check"></v-icon>
                        </template>
                        <v-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                            eiusmod.</v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12" md="6">
                    <v-card elevation="16" append-avatar="https://cdn.vuetifyjs.com/images/john.jpg" class="mx-auto"
                        prepend-avatar="https://cdn.vuetifyjs.com/images/logos/v-alt.svg"
                        subtitle="prepend-avatar and append-avatar" title="Avatars">
                        <v-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                            eiusmod.</v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12" md="6">
                    <v-card elevation="16" class="mx-auto" subtitle="prepend and append" title="Avatars">
                        <template v-slot:prepend>
                            <v-avatar color="blue-darken-2">
                                <v-icon icon="mdi-alarm"></v-icon>
                            </v-avatar>
                        </template>
                        <template v-slot:append>
                            <v-avatar size="24">
                                <v-img alt="John" src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
                            </v-avatar>
                        </template>
                        <v-card-text>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                            eiusmod.</v-card-text>
                    </v-card>
                </v-col>
            </v-row>
</v-app>
  </v-responsive>
    </template>
<script>
import axios from 'axios'
export default {
  
  data: () => ({
      id:'',
      email:'',
      password:'',
      status:'',
      picture:'',
      username:'',
      }),

    async mounted() {
      let user = window.sessionStorage.getItem('email');
      console.log('users=', user);
      const response = await axios.get('http://localhost:7000/listid?email='+ user) ;
          let data = response.data;
          console.log('user=',data.row.username)
          this.email = data.row.email
          this.username = data.row.username
    },
      
  methods: {
      logout() {
          window.sessionStorage.clear();
          this.$router.replace('/login');
      },
  },
};
</script>