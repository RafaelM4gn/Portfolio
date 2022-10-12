<template>
  <div class="box">
    <img class="profile-pic" src="https://avatars.githubusercontent.com/u/40338798?v=4img_avatar.png" alt="Avatar">
  </div>
</template>

<style>

.profile-pic {
  height: 150px;
  border-radius: 50%;
  display: block;
}

.box {
  align-self: center;
  align-items: center;
  padding: 21px;
  position: relative;
  width: 160px;
  height: 160px;
  display: flex;
  justify-content: center;
  background: rgba(0, 0, 0, .5);
  overflow: hidden;
  border-radius: 50%;
  z-index: 0;
  margin-left: auto;
  margin-right: auto;
  margin-top: -50px;
  margin-bottom: -75px;
}

.box::before {
  content: '';
  position: absolute;
  width: 300px;
  height: 200%;
  background: linear-gradient(#00ccff, #d400d4);
  animation: animate 3s linear infinite;
}

.box::after {
  content: '';
  position: absolute;
  inset: 15px;
  background: #272727;
  border-radius: 50%;
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
