<template>
  <div>
    <nuxt-logo/>
    <h2>LOREN IPSUM</h2>
    <h3>LOREN IPSUM</h3>
    <h1 class="gradient2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae fuga quod vitae, unde facere, inventore deleniti quidem, totam tenetur sequi optio dignissimos nulla voluptatum eveniet vero commodi enim eos? Aspernatur. <br> BEM</h1>
    <v-row>
     <h1 class="gradient">TESTE</h1>
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
