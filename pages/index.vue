<template>
  <div>
    <nuxt-logo />
    <v-row>
      <h1 class="gradient">
        TESTE
      </h1>
      <v-card>
        <v-card-tittle>
          Tesntado
        </v-card-tittle>
      </v-card>
      <v-card>
        <v-card-title class="headline">
          Olá, Seja muito bem-vindo 👋
        </v-card-title>
        <v-card-subtitle>
          Sou Rafael, atualmente estou cursando o BTI pela UFRN😎
        </v-card-subtitle>
        <v-card-text>
          - Gosto de muito de tecnologias e tenho sempre vontade de aprender coisas novas. 📚 <br>
        </v-card-text>
        <v-card-actions>
          <v-btn block to="/projects" rounded color="cyan">
            veja meus projetos!
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style>
 #app h1 {
  color: black;
  margin-top: 0rem;
}

.gradient {
  background: linear-gradient(45deg, #FA8BFF 0%, #2BD2FF 52%, #2BFF88 90%);
}

.gradient2 {
  background: linear-gradient(45deg, #eeff00 0%, #2BFF88 90%);
}
</style>
