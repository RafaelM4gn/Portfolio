<template>
  <div>
    <div class="box">
      <h1>hello</h1>
      <h2>RAFAel h2</h2>
      <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est eaque</h3>
    </div>
    <h1>-------------------------------------------------</h1>
    <v-card
      class="mx-auto box"
      max-width="344"
      variant="outlined"
    >
      <v-card-item>
        <div>
          <div class="text-overline mb-1">
            OVERLINE
          </div>
          <div class="text-h6 mb-1">
            Headline
          </div>
          <div class="text-caption">
            Greyhound divisely hello coldly fonwderfully
          </div>
        </div>
      </v-card-item>

      <v-card-actions>
        <v-btn variant="outlined">
          Button
        </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>

</script>

<style>
.box {
  padding: 21px;
  position: relative;
  width: 400px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgba(0, 0, 0, .5);
  overflow: hidden;
  border-radius: 20px;
  z-index: 0;
}

.box::before {
  content: '';
  position: absolute;
  width: 150px;
  height: 200%;
  background: linear-gradient(#00ccff, #d400d4);
  animation: animate 3s linear infinite;
}

.box::after {
  content: '';
  position: absolute;
  inset: 15px;
  background: #272727;
  border-radius: 6px;
}

@keyframes animate {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

.box * {
  position: relative;
  color: #ffffff;
  z-index: 1;
}
</style>
