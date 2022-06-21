<template>
  <div class="player-container">
    <vue-core-video-player src="https://cdn.theguardian.tv/webM/2015/07/20/150716YesMen_synd_768k_vp8.webm" :autoplay="false"></vue-core-video-player>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.player-container {
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}
</style>
