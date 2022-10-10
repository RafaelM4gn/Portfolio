<template>
  <v-container class="pa-4 text-center">
    <v-row
      class="fill-height"
      align="center"
      justify="center"
    >
      <template>
        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
          md="4"
        >
          <!-- card aqui -->
          <v-hover v-slot="{ hover }">
            <v-card
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
            >
              <v-img
                :src="item.img"
                height="225px"
              >
                <v-card-title class="text-h6 white--text">
                  <v-row
                    class="fill-height flex-column"
                    justify="space-between"
                  >
                    <p class="mt-4 subheading text-left">
                      {{ item.title }}
                    </p>

                    <div>
                      <p class="ma-0 text-body-1 font-weight-bold font-italic text-left">
                        {{ item.text }}
                      </p>
                      <p class="text-caption font-weight-medium font-italic text-left">
                        {{ item.subtext }}
                      </p>
                    </div>
                    <v-card-actions>
                      <v-btn
                        :class="{ 'show-btns': hover }"
                        color="teal"
                        rounded
                      >
                        ver no Github
                      </v-btn>
                    </v-card-actions>
                  </v-row>
                </v-card-title>
              </v-img>
            </v-card>
          </v-hover>
          <!-- fim do card -->
        </v-col>
      </template>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    icons: ['mdi-rewind', 'mdi-play', 'mdi-fast-forward'],
    items: [
      {
        title: 'Projeto 1',
        text: 'subtitulo',
        subtext: 'Loren ipsum dolor no sit amet',
        img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80'
      },
      {
        title: 'Projeto 2',
        text: 'subtitulo',
        subtext: 'Loren ipsum dolor no sit amet',
        img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80'
      },
      {
        title: 'Projeto 3',
        text: 'subtitulo',
        subtext: 'Loren ipsum dolor no sit amet',
        img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80'
      },
      {
        title: 'Projeto 3',
        text: 'subtitulo',
        subtext: 'Loren ipsum dolor no sit amet',
        img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80'
      },
      {
        title: 'Projeto 3',
        text: 'subtitulo',
        subtext: 'Loren ipsum dolor no sit amet',
        img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80'
      }
    ],
    transparent: 'rgba(255, 255, 255, 0)'
  })
}
</script>

<style scoped>
.v-card {
  transition: opacity .4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
 }

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>
