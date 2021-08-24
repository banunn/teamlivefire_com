<template>
  <v-app light>
    <v-app-bar :color="bg" height="90px" flat hide-on-scroll fixed app>
      <NuxtLink to="/">
        <img class="logo" src="~/assets/logo.svg" alt="" />
      </NuxtLink>
      <v-spacer />
      <v-btn text to="/support">Support</v-btn>
      <v-btn
        depressed
        tag="a"
        href="https://access.teamlivefire.com/manage/"
        target="blank"
        color="black"
        class="ml-4 white--text"
        >Log In</v-btn
      >
    </v-app-bar>
    <v-main :class="{ 'pt-md-0': routeName === '/' }">
      <Nuxt />
    </v-main>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      bg: 'transparent',
    }
  },
  mounted() {
    window.onscroll = () => {
      this.changeColor()
    }
  },
  methods: {
    changeColor() {
      if (
        document.body.scrollTop > 100 ||
        document.documentElement.scrollTop > 100
      ) {
        this.bg = 'white'
      } else {
        this.bg = 'transparent'
      }
    },
  },
  computed: {
    routeName() {
      return this.$route.path
    },
  },
}
</script>

<style scoped lang="scss">
.logo {
  width: 212px;
}
</style>
