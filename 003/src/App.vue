<template>
  <v-app>
    <Sidebar />

    <v-main>
      <HomeComponent />
    </v-main>
  </v-app>
</template>

<script>
import Sidebar from './components/SideBar.vue'
import HomeComponent from './components/HomeComponent.vue'

export default {
  name: 'App',

  components: {
    Sidebar,
    HomeComponent
  },

  data: () => ({
    //
  }),
};
</script>
