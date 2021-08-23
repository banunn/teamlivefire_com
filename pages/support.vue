<template>
  <v-row>
    <h1 class="text-center" v-text="count"></h1>
    <v-btn @click="count += 1">Increment</v-btn>
  </v-row>
</template>

<script>
export default {
  name: 'support_page',
  data: () => ({
    count: 3,
  }),
}
</script>

<style lang="scss" scoped></style>
