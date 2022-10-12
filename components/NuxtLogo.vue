<template>
  <div class="vue-logo">
    <h1>RafaelM4gn</h1>
  </div>
</template>

<style>

.vue-logo h1 {
  display: block;
  margin: auto;
  height: 60px;
  background-image: linear-gradient(124deg, #1de840, #284ec0, #dd00f3);
  background-size: 1000% 1000%;
  font-size: 45px;
  text-align: center;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  filter: drop-shadow(0px 3px 2px rgba(0, 0,0, .1));
  animation: rainbow 19s ease infinite;
}

@keyframes rainbow {
  0% {
    background-position: 0% 0%
  }

  50% {
    background-position: 60% 0%
  }

  100% {
    background-position: 0% 0%
  }
}
</style>
