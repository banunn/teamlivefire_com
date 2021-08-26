<template>
  <div class="row block" :class="{ 'flex-row-reverse': reverse }">
    <v-col class="center" md="5" sm="12">
      <div class="copy" style="justify-content: flex-end !important">
        <h2 class="text-headline" v-text="headline"></h2>
        <p class="body-copy" v-text="body"></p>
      </div>
    </v-col>
    <v-col md="7" sm="12">
      <v-img :src="img + '?nf_resize=smartcrop&w1000'"></v-img>
    </v-col>
  </div>
</template>

<script>
export default {
  name: 'feature_block',
  props: {
    headline: {
      type: String,
      required: true,
    },
    body: {
      type: String,
      required: true,
    },
    img: {
      type: String,
      required: true,
    },
    reverse: {
      type: Boolean,
      required: false,
    },
  },
}
</script>

<style lang="scss" scoped>
.center {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  .copy {
    width: 65%;
    @media (max-width: 1000px) {
      width: calc(85% - 24px);
      margin: 0 auto;
      text-align: center;
    }
  }
}
.subline {
  font-size: 14px;
  text-transform: uppercase;
  font-weight: 400;
  margin-bottom: 36px;
}

.text-headline {
  font-size: 40px;
  line-height: 1.5em;
  text-transform: uppercase;
  font-weight: 300;
}

.head-copy {
  letter-spacing: 0.08em;
  line-height: 1.8em;
  font-size: 24px;
}
.body-copy {
  font-size: 16px;
  line-height: 1.8em;
}
</style>
