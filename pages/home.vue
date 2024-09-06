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
        src="https://static1.topspeedimages.com/wordpress/wp-content/uploads/2022/09/a10.jpeg"
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
        src="https://cdn.visordown.com/styles/xl/s3/field/image/top-gun-maverick-h2-scene.jpeg?itok=S2g-TogB"
        contain
        class="custom-carousel-item"
      ></v-img>
    </v-carousel-item>
    <v-carousel-item>
      <v-img
        src="https://d1uzk9o9cg136f.cloudfront.net/f/16783100/rc/2022/05/24/0205d395e73f38b04cf21607e15e6eb4976a0971_xlarge.jpg"
        contain
        class="custom-carousel-item"
      ></v-img>
    </v-carousel-item>
  </v-carousel>
  <v-row align="center" justify="center" dense>
                <v-col cols="12 pt-3" md="6">
                    <v-card elevation="16" append-avatar="https://logowik.com/content/uploads/images/kawasaki1827.logowik.com.webp" class="mx-auto"
                     prepend-avatar="https://ae01.alicdn.com/kf/S9aa446850c25477d84d58051ab90c3ddY/Fairing.png"
                        subtitle="รถซุปเปอร์ไบค์ที่เเรงที่สุดในโลก" title="Kawasaki Ninja H2®">
                        <v-card-text>ทีเด็ดของมอเตอร์ไซค์ต้นแบบรุ่นนี้อยู่ที่เครื่องยนต์ 4 สูบ ขนาด 998 ซีซี ที่ติดตั้งซูเปอร์ชาร์จ ให้กำลัง 300 แรงม้า ตัวซุปเปอร์ชาร์จรับลมจากช่องลมด้านหน้า เพื่อเพิ่มกำลังของเครื่องยนต์ โดยคาวาซากิตั้งใจให้มันสามารถทำความเร็วถึง 320 กม./ชม. ได้แบบสบาย ๆ
                        </v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12 pt-3" md="6">
                    <v-card elevation="16" class="mx-auto" subtitle=" Shogo Kawasaki (โชโซ คาวาซากิ)" title="ผู้ก่อตั้งบริษัท Kawasaki">
                        <template v-slot:prepend>
                            <v-icon color="green" icon="mdi-motorbike"></v-icon>
                        </template>
                        <v-card-text>คาวาซากิ (Kawasaki) ผู้ผลิตมอเตอร์ไซค์รายใหญ่ เผยโฉมมอเตอร์ไซค์สปอร์ตรุ่นใหม่ 
                        ซึ่งจัดเต็มเทคโนโลยีและการออกแบบใหม่ล่าสุดที่ล้ำสมัยอย่างน่าทึ่งกับ คาวาซากิ นินจา เอช2อาร์ (Kawasaki Ninja H2R) บิ๊กไบค์ทรงสปอร์ตเรซซิ่งรุ่นใหม่ล่าสุดของปี 2014 </v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12" md="6">
                    <v-card elevation="16" append-avatar="https://1000logos.net/wp-content/uploads/2022/11/Top-Gun-Logo-1986.png" class="mx-auto"
                        prepend-avatar="https://ae01.alicdn.com/kf/H29c1bb710e5648e094f08cf5445d8549E/For-Kawasaki-GPZ-900R-GPZ900r-Motorcycle-body-Wheels-Fairing-Helmet-Tank-Pad-decoration-logo-Label-reflective.jpg"
                        subtitle="รถรุ่นพี่ต้นกำเนิดของ Kawasaki Ninja H2®" title="Kawasaki GPZ900®">
                        <v-card-text>GPZ900R มันคือรถมอไซต์รุ่นพี่ต้นกำเนิดของ Kawasaki Ninja H2R จักรยานยนต์ที่ผลิตโดย Kawasaki ตั้งแต่ปี 1984 ถึง 2003 เป็นสมาชิกรุ่นแรกสุดของตระกูล Ninja ของสปอร์ตไบค์ GPZ900R รุ่นปี 1984 เป็นดีไซน์ที่ปฏิวัติวงการซึ่งกลายมาเป็นรุ่นก่อนหน้าของรถสปอร์ตไบค์ยุคใหม่ </v-card-text>
                    </v-card>
                </v-col>

                <v-col cols="12" md="6">
                    <v-card elevation="16" class="mx-auto" subtitle="จากบริษัทขายเรือประมงสู่บริษัทขายรถที่ดีที่สุดตลอดกาลของโลก" title="ต้นกำเนิดของบริษัท kawasaki">
                        <template v-slot:prepend>
                            <v-avatar color="green">
                                <v-icon icon="mdi-home"></v-icon>
                            </v-avatar>
                        </template>
                        <template v-slot:append>
                            <v-avatar size="24">
                                <v-img alt="John" src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
                            </v-avatar>
                        </template>
                        <v-card-text>ย้อนกลับไปในปี 1878 หรือ 139 ปีที่แล้ว Shozo Kawasaki เป็นผู้ก่อตั้งบริษัทนี้ขึ้นมา เริ่มจากตั้งบริษัทผลิตเรือก่อนโดยใช้ชื่อว่า Kawasaki Tsukiji Shipyard 
                        ซึ่งตั้งอยู่ที่ที่คนไทยรู้จักกันเป็นอย่างดี นั่นก็คือตลาดปลาซึกิจิที่เราไปดูเค้าประมูลปลา และต่อแถวรอกินปลาดิบสด ๆ นั่นเอง</v-card-text>
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