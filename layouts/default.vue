<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <div>
        <nuxt-logo />
      </div>
      <!-- <h1 >RAFAEL MAGNO</h1> -->
      <v-tabs
        v-model="tab"
        color="deep-purple-accent-4"
        right
      >
        <v-tab v-for="(item, i) in items" :key="i" :to="item.to" :value="i">
          {{ item.title }}
        </v-tab>
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
          title: 'HOME',
          to: '/'
        },
        {
          title: 'PROJECTS',
          to: '/projects'
        },
        {
          title: 'THREE',
          to: '/threejs'
        },
        {
          title: 'CONTACT',
          to: '/contact'
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

@import url('https://fonts.googleapis.com/css2?family=Fira+Code&display=swap');

#app {
  background-image: linear-gradient(135deg, #1de840, #284ec0, #dd00f3);
  background-size: 300% 300%;
  animation: rainbow 19s ease infinite;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  @keyframes rainbow {
    0% {
      background-position: 0% 0%
    }

    50% {
      background-position: 100% 0%
    }

    100% {
      background-position: 0% 0%
    }
  }
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
