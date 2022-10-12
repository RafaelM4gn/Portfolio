<template>
  <div>
    <v-responsive min-height="25vh" />
    <div>
      <profile-picture />
      <div class="card-profile">
        <h1>
          Rafael Magno
        </h1>
        <h2 style="padding-top: 8px">
          Graduating in Information Technology - <strong> UFRN</strong>
        </h2>
        <div style="padding-bottom: 15px">
          <h2>
            <v-icon>
              mdi-map-marker-outline
            </v-icon>
            <strong>
              Natal, Brasil
            </strong>
          </h2>
        </div>
        <p style="padding-bottom: 30px">
          <v-icon normal color="white">
            mdi-email-outline
          </v-icon>
          rfl.magno02@gmail.com
        </p>
        <v-btn
          v-for="(item, i ) in media"
          :key="i"
          style="text-align: end"
          :href="item.link"
          target="_blank"
          class="ma-2 card-icon"
          text
          x-large
          icon
        >
          <v-icon class="card-icon" large>
            {{ item.icons }}
          </v-icon>
        </v-btn>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    media: [
      {
        icons: 'mdi-github',
        link: 'https://github.com/rafaelm4gn'
      },
      {
        icons: 'mdi-instagram',
        link: 'https://instagram.com/rfl.magno02/'
      },
      {
        icons: 'mdi-file-account-outline',
        link: 'https://www.canva.com/design/DAFG0vzZ-FI/NthQ0NY4tFxKEfGHuXQykg/view?utm_content=DAFG0vzZ-FI&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton'
      },
      {
        icons: 'mdi-linkedin',
        link: 'https://www.linkedin.com/in/rafael-magno-bb47401b8/'
      }
    ]
  })
}

</script>

<style>
.card-icon{
  background-image: linear-gradient(135deg, #1de840, #284ec0, #dd00f3);
  background-size: 1000% 1000%;
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: rainbow 19s ease infinite;
}

.card-profile h1 {
  margin-left: auto;
  margin-right: auto;
  height: 60px;
  background-image: linear-gradient(135deg, #1de840, #284ec0, #dd00f3);
  background-size: 1000% 1000%;
  font-size: 45px;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  animation: rainbow 19s ease infinite;
}

.card-profile h2 {
  font-weight: normal;
  color: #fff;
}

.card-profile {
  padding-top: 80px;
  padding-left: 50px;
  padding-right: 50px;
  text-align: center;
  background-color: #272727;
  height: 400px;
  width: 600px;
  flex-grow: 0;
  flex-shrink: 0;
  flex-basis: 50%;
  border-radius: 20px;
}
</style>
