<template>
  <div class="my-5 line-tag">
    <span class="mx-3 color-theme font-weight-bold">{{ text }}</span>
  </div>
</template>

<script>
export default {
  props: ['text']
}
</script>

<style lang="scss" scoped>
.line-tag {
  border-left: 5px solid #635f98;
}
</style>
