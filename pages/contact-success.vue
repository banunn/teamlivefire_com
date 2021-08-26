<template>
  <div class="page">
    <v-parallax dark height="350" :src="require('~/assets/support-bg.webp')">
      <div class="overlay"></div>
      <div class="wrap">
        <div class="copy-block">
          <div class="copy">
            <h3 class="text-headline text-center">Support</h3>
          </div>
        </div>
      </div>
    </v-parallax>
    <div class="wrap">
      <h1 class="text-center">We've Recieved Your Request</h1>
      <p>
        Thank you for getting in touch. We will provide a response as quickly as
        possible
      </p>
      <div class="row justify-center pa-8">
        <v-btn
          @click="goHome"
          elevation="0"
          large
          color="black"
          class="white--text"
          >Back Home</v-btn
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'contact_success_page',
  methods: {
    goHome() {
      return this.$router.push('/')
    },
  },
}
</script>

<style lang="scss" scoped>
.wrap {
  margin: 0 auto;
  padding: 48px 24px;
  max-width: 680px;
}
</style>
