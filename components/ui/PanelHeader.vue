<template>
  <div class="d-flex justify-space-between align-center my-6">
    <h2 class="color-theme font-weight-bold font-32" data-aos="fade-down">{{ title }}</h2>
    <div>
      <small class="mx-2 grey--text font-16">ดูทั้งหมด</small>
      <v-btn elevation="1" fab x-small color="white">
        <v-icon> mdi-chevron-right </v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  props: ['title'],
  mixins: [aosMixin]
}
</script>
