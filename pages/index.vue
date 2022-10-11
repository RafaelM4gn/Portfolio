<template>
  <div>
    <v-responsive min-height="30vh" />
    <v-divider class="divider" />
    <h1 class="intro">
      Hello, I'm
    </h1>
    <h1 class="myname">
      RAFAEL MAGNO
    </h1>
    <h1 class="outro">
      A Full Stack Developer
    </h1>
    <v-divider class="divider" />
    <div class="subh">
      <h1>
        Check out my projects
      </h1>
      <v-spacer />
      <h1>-></h1>
      <v-spacer />
      <v-btn
        class="divider"
        outlined
        x-large
        color="#fff"
        to="/projects"
      >
        PROJECTS
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style>
h1{
  font-weight: 700;
  font-family: 'Fira Code', monospace;
}

h2 {
  padding-left: 9px;
  font-size: large;
  font-weight: 800;
  font-family: 'Fira Code', monospace;
  color: #272727;
}

.divider {
  border-width: 3px;
  height: 700px;
}

.subh {
  display: flex;
  text-align: center;
  padding-top: 10px;
}

.intro {
  color: #272726;
  text-align: left;
  font-size: 35px;
}

.myname {
  margin-top: -30px;
  margin-bottom: -30px;
  color: #fff;
  text-align: justify;
  font-size: 100px;
}

.outro {
  color: #272726;
  text-align: right;
  font-size: 35px;
}
.gradient {
  background: linear-gradient(45deg, #FA8BFF 0%, #2BD2FF 52%, #2BFF88 90%);
}

.gradient2 {
  background: linear-gradient(45deg, #eeff00 0%, #2BFF88 90%);
}
</style>
