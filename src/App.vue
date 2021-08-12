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
      
      <div class="text-center">
    <v-menu
      open-on-hover
      top
      offset-y
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          text
          v-bind="attrs"
          v-on="on"
        >
          <span class="mr-2"> username </span>
          <v-icon> {{ downcropIcon }} </v-icon>
        </v-btn>
      </template>

      <v-list>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          @click="item.method"
        >
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
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
    items: [
      { title: "My Profile", method: () => {
        console.log("My Profile")
      }},
      { title: "My Submissions", method: () => {
        routeTo("/submissions?user={{ username }}")
      }},
      { title: "Logout", method: () => {
        console.log("Logout")
      }},
    ]
  }),
};
</script>
