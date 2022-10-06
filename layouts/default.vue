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
          class="ma-2"
          rounded
          to="/"
          outlined
          color="teal"
          @click.stop="rightDrawer = !rightDrawer"
        >
          HOME
        </v-btn>
        <v-btn
          class="mx-1"
          rounded
          to="/projects"
          outlined
          color="teal"
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

  // background-image: linear-gradient(90deg, #9572FC 0%, #43E7AD 50.52%, #E2D45C 100%);
  background-image: linear-gradient(124deg, #1de840, #2b1de8, #dd00f3);
  background-size: 100% 100%;
  animation: rainbow 18s ease infinite;

  @keyframes rainbow {
    0% {
      background-position: 0% 0%
    }

    50% {
      background-position: 100% 19%
    }

    100% {
      background-position: 0% 0%
    }
  }

  // #tabs  {
  // background-color: #EDEDED;
  // }
}
</style>
