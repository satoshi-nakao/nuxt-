<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>Navigation Lists</v-navigation-drawer>
    <v-app-bar color="dark"  app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>My Page</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
      <v-btn  v-for="item in items" :key="item">{{ item.name }}</v-btn>
      </v-toolbar-items>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer  dark app>
      Vuetify
    </v-footer>
  </v-app>
</template>zz

<script>
export default {
  data(){
    return{
      drawer: false,
      items: [
        {name: 'Profile',},
        {name: 'Works'},
        {name: 'Skil'},
        {name: 'Contact'}
      ]
    }
  }
}
</script>