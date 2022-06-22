<template>
  <div class="my-5 line-tag">
    <span class="mx-3 color-theme font-weight-bold" data-aos="fade-down">{{ text }}</span>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  props: ['text'],
  mixins: [aosMixin]
}
</script>

<style lang="scss" scoped>
.line-tag {
  border-left: 5px solid #635f98;
}
</style>
