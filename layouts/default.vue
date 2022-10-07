<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
       <v-app-bar-title >RAFAELM4GN</v-app-bar-title>
       <!-- <h1 >RAFAEL MAGNO</h1> -->
      <v-tabs v-model="tab" color="deep-purple-accent-4" right>
        <v-tab to="/" :value="1">HOME</v-tab>
        <v-tab to="/projects" :value="2">PROJETOS</v-tab>
      </v-tabs>
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
  background-image: linear-gradient(124deg, #1de840, #2b1de8, #dd00f3);
  background-size: 300% 300%;
  animation: rainbow 18s ease infinite;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
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
}

#app h1 {
  color: black;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  filter: drop-shadow(0px 3px 2px rgba(0, 0,0, .1));
  margin-top: -7rem;
}

#app v-app-bar-title {
  color: black;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  filter: drop-shadow(0px 3px 2px rgba(0, 0,0, .1));
  margin-top: -7rem;
}

.gradient {
  background: linear-gradient(45deg, #FA8BFF 0%, #2BD2FF 52%, #2BFF88 90%);
}

</style>
