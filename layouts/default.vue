<template>
  <v-app >
    <v-card 
    color="grey-darken-4"
    >
      <v-layout>
        ///
        <v-system-bar color="green darken-1" >
          <v-icon class="ms-2" icon="mdi-wifi-strength-4 " color="white darken-1"></v-icon>
        <v-icon class="ms-2" icon="mdi-signal-cellular-outline" color="yellow darken-1"></v-icon>
          <v-icon class="ms-2" icon="mdi-battery" color="red darken-1"></v-icon>
          <span class="ms-2" >12:30 </span> 
        </v-system-bar>
        ///
        <v-app-bar
          :elevation="22" 
          image="https://imgv3.fotor.com/images/share/Free-blue-gradient-pattern-background-from-Fotor.jpg"
          gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
        >

          <template v-slot:prepend>
            <v-app-bar-nav-icon></v-app-bar-nav-icon>
          </template>
          <v-app-bar-title>C - Probigbike</v-app-bar-title>
          <v-spacer></v-spacer>
          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-account</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </v-app-bar>
        <v-navigation-drawer
          color="blue-grey darken-4"
          v-model="drawer"
          :rail="rail"
          permanent
          @click="rail = false"
        >
          <v-list-item
            
            prepend-avatar="\assets\image\888.jpg"
            title="Warinthon Nanthaboonma"
            nav
          >
            <template v-slot:append>
              <v-btn
                icon="mdi-chevron-left"
                variant="text"
                @click.stop="rail = !rail"
              ></v-btn>
            </template>
          </v-list-item>
          <v-divider></v-divider>
          <v-list density="compact" nav>
            <v-list-item
              prepend-icon="mdi-home-city"
              title="หน้าหลัก"
              value="home"
              @click="main"
            ></v-list-item>
            <v-list-item
           
              prepend-icon="mdi-plus"
              size="x-large"
              title="เพิ่มข้อมูล"
              value="add"
              @click="add"
            ></v-list-item>
            <v-list-item
              prepend-icon="mdi-home-city"
              title="แสดงข้อมูล"
              value="home"
              @click="listdata"
            ></v-list-item>
            <v-list-item
              prepend-icon="mdi-account"
              title="เกี่ยวกับ"
              value="deboard"
              @click="deboard"
            ></v-list-item>
            <v-list-item
              prepend-icon="mdi-close-circle"
              title="LOGOUT"
              value="users"
              @click="logOut"
            ></v-list-item>
          </v-list>
        </v-navigation-drawer>
        <!-- <v-main style="height: 650px"></v-main> -->
        <v-main  
         color=""
        >
         <NuxtPage ></NuxtPage>
          <!-- Main Content -->
        </v-main>
        <!--  -->

        <v-bottom-navigation v-model="value" :bg-color="color" mode="shift">
          <v-btn>
            <v-icon>mdi-television-play</v-icon>

            <span>Video</span>
          </v-btn>

          <v-btn>
            <v-icon>mdi-music-note</v-icon>

            <span>Music</span>
          </v-btn>

          <v-btn>
            <v-icon>mdi-book</v-icon>

            <span>Book</span>
          </v-btn>

          <v-btn>
            <v-icon>mdi-image</v-icon>

            <span>Image</span>
          </v-btn>
        </v-bottom-navigation>
      </v-layout>
    </v-card>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      drawer: true,
      rail: true,
      username: '',
      email: '',
    };
  },
  async mounted() {
      let user = window.sessionStorage.getItem('email');
      console.log('users=', user);
      if (!user) { // user is null
          this.$router.replace('/login')
          return
      }
  },

  methods: {
    main(){
      this.$router.replace("/home");
    },
    listdata(){
      this.$router.replace("/show");
    },
    showdata(){
      this.$router.replace("/account");
    },
    deboard(){
      this.$router.replace("/deboard");
    },
    add(){
      this.$router.replace("/add");
    },
    logOut() {
      window.sessionStorage.clear();
      this.$router.replace("/login");
    },
  },
  
};

</script>