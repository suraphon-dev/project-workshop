<template>
  <div>
    <panel-slide-banner />
    <div class="background-content">
      <panel-article-news />
    </div>
    <panel-channel />
    <panel-content-slide />
  </div>
</template>

<script>
import PanelSlideBanner from '~/components/PanelSlideBanner.vue'
import PanelArticleNews from '~/components/PanelArticleNews.vue'
import PanelChannel from '~/components/PanelChannel.vue'
import PanelContentSlide from '~/components/PanelContentSlide.vue'

export default {
  components: {
    PanelSlideBanner,
    PanelArticleNews,
    PanelChannel,
    PanelContentSlide
  }
}
</script>

<style lang="scss" scoped>
.background-content {
  height: 155vh;
  background-image: url('assets/images/bg-component-news.jpg');
  background-size: 100%;
  object-fit: cover;
  margin-top: 75px;
  @media (max-width: 960px) {
    background-size: unset;
    height: unset;
    background-image: unset;
  }
}
</style>
