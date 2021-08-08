<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      dense
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
         <v-icon> {{ homeIcon }} </v-icon>
          <span class="mr-2">Home</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
         <v-icon> {{ problemIcon }} </v-icon>
          <span class="mr-2">Problemset</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
         <v-icon> {{ contestIcon }} </v-icon>
          <span class="mr-2">Contest</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
         <v-icon> {{ trainIcon }} </v-icon>
          <span class="mr-2">Train</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <v-icon> {{ statusIcon }} </v-icon>
          <span class="mr-2">Status</span>
        </v-btn>
      </div>

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <v-icon> {{ accountIcon }} </v-icon>
          <span class="mr-2">Users</span>
        </v-btn>
      </div>

      <v-spacer />

      <div class="d-flex align-center">
        <v-btn
         text
         >
          <span class="mr-2"> username </span>
          <v-icon> {{ downcropIcon }} </v-icon>
        </v-btn>
      </div>
      


    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

// find icons here: https://material.iconhelper.cn/ 
import { mdiChevronDown, mdiDumbbell, mdiHistory } from '@mdi/js';
import { mdiAccount, mdiHome, mdiFormatListBulletedSquare, mdiCalendarCheck} from '@mdi/js'

export default {
  name: 'App',

  data: () => ({
    downcropIcon: mdiChevronDown,
    accountIcon:  mdiAccount,
    homeIcon: mdiHome,
    problemIcon: mdiFormatListBulletedSquare,
    contestIcon: mdiCalendarCheck,
    trainIcon: mdiDumbbell,
    statusIcon: mdiHistory,

    //
  }),
};
</script>
