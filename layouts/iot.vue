<template>
    <v-app>
      <v-layout class="rounded rounded-md">
        <!-- Top App Bar -->
        <v-app-bar color="surface-variant" title="C-PROBIKE"></v-app-bar>
  
        <!-- Navigation Drawer -->
        <v-navigation-drawer>
          <v-list>
            <v-list-item>
              <v-card class="mx-auto" max-width="500">
                <v-card-title>
                  อื่น
                </v-card-title>
                <div>
                  <v-btn variant="tonal" block class="temperature-btn">
                    อุณหภูมิ
                  </v-btn>
                  <br>
                  <v-btn variant="tonal" block class="smart-home-btn">
                    สมาร์ทโฮม
                  </v-btn>
                  <br>
                  <v-btn variant="tonal" block class="smart-frame-btn">
                    สมาร์ทเฟรม
                  </v-btn>
                </div>
              </v-card>
            </v-list-item>
          </v-list>
        </v-navigation-drawer>
  
        <!-- Main Content Area -->
        <v-main class="main-content">
          <NuxtPage />
          <!-- Main Content -->
        </v-main>
  
      </v-layout>
    </v-app>
  </template>
  
  <style>
  .temperature-btn {
    background-color: red;
    color: #fff;
  }
  
  .smart-home-btn {
    background-color: orange;
    color: #fff;
  }
  
  .smart-frame-btn {
    background-color: green;
    color: #fff;
  }
  
  .main-content {
    min-height: 300px;
    background: #ffbf00 url('https://full.life/media/magefan_blog/R6_Y9S1.jpg') no-repeat center center;
    background-size: cover;
  }
  </style>
  