<template>
  <v-row>
    <v-img
      :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
      aspect-ratio="1"
      class="grey lighten-2"
    >
      <template #placeholder>
        <v-row
          class="fill-height ma-0"
          align="center"
          justify="center"
        >
          <v-progress-circular
            indeterminate
            color="grey lighten-5"
          />
        </v-row>
      </template>
    </v-img>
    <v-card>
      <v-card-title class="headline">
        Olá, Seja muito bem-vindo 👋
      </v-card-title>
      <v-card-subtitle>
        Sou Rafael, atualmente estou cursando o BTI pela UFRN😎
      </v-card-subtitle>
      <v-card-text>
        - Gosto de muito de tecnologias e tenho sempre vontade de aprender coisas novas. 📚 <br>
        - Tenho uma namorada incrivel 💖
      </v-card-text>
      <v-card-actions>
        <v-btn block to="/projects" rounded color="cyan">
          veja meus projetos!
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
