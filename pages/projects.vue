<template>
  <v-container class="pa-4 text-center">
    <h1 class="mb-4 cool">MY GITHUB REPOSITORYS</h1>
    <v-row
      class="fill-height"
      align="center"
      justify="center"
    >
      <v-col
        v-for="(item, i) in repos"
        :key="i"
        cols="12"
        md="4"
      >
        <!-- card aqui -->
        <v-hover v-slot="{ hover }">
          <v-card
            style="border-radius: 20px"
            :elevation="hover ? 24 : 2"
            :class="{ 'on-hover': hover }"
            height="225px"
          >
            <v-card-title class="text-h6 white--text">
              <v-row
                class="fill-height d-flex flex-column"
                justify="space-between"
              >
                <h3 class="my-4 mx-3 text-left">
                  {{ item.name }}
                </h3>

                <div>
                  <p class="ma-0 mx-3 text-body-1 font-weight-normal font-italic text-left">
                    {{ item.description }}
                  </p>
                  <p class="text-caption font-weight-medium font-italic text-left">
                    <!-- {{ item.subtext }} -->
                  </p>
                </div>
              </v-row>
            </v-card-title>
            <v-spacer />
            <v-card-actions>
              <v-btn
                absolute
                bottom
                right
                :href="item.html_url"
                target="_blank"
                :class="{ 'show-btns': hover }"
                color="teal"
                rounded
              >
                <v-icon class="mr-2">
                  mdi-github
                </v-icon>
                ver no Github
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-hover>
        <!-- fim do card -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import axios from 'axios'

export default {
  data: () => ({
    icons: ['mdi-rewind', 'mdi-play', 'mdi-fast-forward'],
    img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80',
    transparent: 'rgba(255, 255, 255, 0)',
    repos: null
  }),
  created: function () {
    axios.get('https://api.github.com/users/RafaelM4gn/repos').then((response) => {
      this.repos = response.data
    })
  }
}
</script>

<style scoped>
.options {
  margin-bottom: 15px;
  position: absolute;
}
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.8;
 }

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>
