<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <h1>RAFAEL MAGNO</h1>
      <v-spacer />
      <div class="text-center mx-2">
        <v-btn
          class="mx-1"
          rounded
          to="/"
          outlined
          @click.stop="rightDrawer = !rightDrawer"
        >
          HOME
        </v-btn>
        <v-btn
          class="mx-1"
          rounded
          to="/projects"
          outlined
          @click.stop="rightDrawer = !rightDrawer"
        >
          PROJETOS
        </v-btn>
     </div>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style lang="scss" scoped>

#app {
  // background-color: #CB997E;

  // #tabs  {
    // background-color: #EDEDED;
  // }
}
</style>
