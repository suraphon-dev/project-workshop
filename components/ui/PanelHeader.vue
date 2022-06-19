<template>
  <div class="d-flex justify-space-between align-center my-6">
    <h2>{{ title }}</h2>
    <div>
      <small class="mx-2">ดูทั้งหมด</small>
      <v-btn elevation="2" fab x-small color="white">
        <v-icon> mdi-chevron-right </v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title']
}
</script>

<style lang="scss" scoped></style>
