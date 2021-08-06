<template>
  <v-app>
    <v-app-bar
      app
      color="white"
    >
      <div class="d-flex align-center">
        <v-btn
         href="https://trswnca.top/coj"
         text
         >
          <span class="mr-2">COJ</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2">首页</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2">题库</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2">比赛</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2">训练</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2">评测</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2">用户</span>
        </v-btn>
      </div>

      <v-spacer />

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2"> username </span>
          <v-icon> {{ downcrop }} </v-icon>
        </v-btn>
      </div>
      


    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

import { mdiChevronDown } from '@mdi/js';

export default {
  name: 'App',

  data: () => ({
    downcrop: mdiChevronDown
    //
  }),
};
</script>
