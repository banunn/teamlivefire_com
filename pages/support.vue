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
    <div class="wrap"><h2 style="font-weight: 300">HOW CAN WE HELP?</h2></div>
    <v-form
      method="POST"
      data-netlify-honeypot="bot-field"
      data-netlify="true"
      name="support-form"
      action="/contact-success"
      netlify
      class="form"
    >
      <v-text-field
        v-model="first"
        name="First Name"
        outlined
        label="First Name"
      ></v-text-field>
      <v-text-field
        v-model="last"
        name="Last Name"
        outlined
        label="Last Name"
      ></v-text-field>
      <v-text-field
        :rules="rules"
        v-model="email"
        outlined
        name="email"
        label="Email"
      ></v-text-field>
      <v-text-field
        v-model="phone"
        name="phone"
        outlined
        label="Phone"
      ></v-text-field>
      <v-textarea
        outlined
        name="comments"
        label="Comments"
        placeholder="Anything you'd like us to know?"
        value=""
        v-model="comments"
      ></v-textarea>
      <div class="row justify-end">
        <v-btn
          :disabled="!comments.length"
          large
          color="black"
          class="white--text"
          type="submit"
          >Submit</v-btn
        >
      </div>
      <input type="hidden" name="form-name" value="support-form" />
    </v-form>
    <div style="border-top: 1px solid #000; margin-top: 48px">
      <lf-support class="wrap-lg"></lf-support>
    </div>
  </div>
</template>

<script>
import lfSupport from '@/components/home/home-support'

export default {
  name: 'support_page',
  components: { lfSupport },
  data: () => ({
    first: '',
    last: '',
    email: '',
    phone: '',
    comments: '',
    rules: [
      (value) => {
        const pattern =
          /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
        return pattern.test(value) || 'Invalid e-mail.'
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.wrap-lg {
  max-width: 1632px;
  padding: 0 16px;
  margin: 88px auto;
}
.text-headline {
  font-size: 40px;
  line-height: 1.5em;
  text-transform: uppercase;
  font-weight: 300;
}
.overlay {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 20px;
  left: 0;
  background: rgba(#000, 0.2);
}
.wrap {
  position: relative;
  margin: 0 auto;
  padding: 48px 24px 0 24px;
  max-width: 680px;
}
.form {
  margin: 0 auto;
  padding: 48px 24px;
  max-width: 680px;
}
</style>
