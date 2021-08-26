<template>
  <v-app light>
    <v-app-bar :color="bg" height="90px" flat hide-on-scroll fixed app>
      <NuxtLink to="/">
        <img class="logo" src="~/assets/logo.svg" alt="" />
      </NuxtLink>
      <v-spacer />
      <div class="nav-links d-none d-md-block">
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
      </div>
      <v-app-bar-nav-icon
        class="d-none d-sm-block d-md-none"
        @click="drawer = true"
      >
      </v-app-bar-nav-icon>
    </v-app-bar>
    <v-navigation-drawer absolute right v-model="drawer" temporary width="80%">
      <div class="row justify-end" style="padding: 24px 16px">
        <v-btn @click="drawer = false" icon elevation="0" large
          ><v-icon>mdi-close</v-icon></v-btn
        >
      </div>
      <v-list>
        <v-list style="text-align: center">
          <v-list-item to="/">
            <v-list-item-content>
              <v-list-item-title>Home</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item to="/support">
            <v-list-item-content>
              <v-list-item-title>Support</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item
            href="https://access.teamlivefire.com/manage/"
            target="_blank"
          >
            <v-list-item-content>
              <v-list-item-title>Log In</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-list>
    </v-navigation-drawer>
    <v-main :class="{ 'pt-md-0': routeName === '/' }">
      <Nuxt />
    </v-main>
    <v-footer absolute dark app class="black">
      <v-card
        class="pa-8 white--text text-center black"
        style="width: 100%"
        flat
        tile
      >
        <div class="row justify-space-between">
          <span>&copy; LiveFire, LLC {{ new Date().getFullYear() }}</span>
          <div class="links">
            <NuxtLink to="/termsandconditions" tag="a" class="white--text"
              >Terms &amp; Conditions</NuxtLink
            >
            |
            <NuxtLink to="/privacypolicy" tag="a" class="white--text"
              >Privacy Policy</NuxtLink
            >
          </div>
        </div>
      </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      bg: 'transparent',
      drawer: false,
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

.v-application {
  font-family: 'Industry', Arial, Helvetica, sans-serif;
}
</style>
