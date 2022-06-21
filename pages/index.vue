<template>
  <div>
    <panel-slide-banner />
    <div class="background-content">
      <panel-slide-subject />
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
import PanelSlideSubject from '~/components/PanelSlideSubject.vue'
import PanelContentSlide from '~/components/PanelContentSlide2.vue'

export default {
  components: {
    PanelSlideBanner,
    PanelArticleNews,
    PanelChannel,
    PanelSlideSubject,
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
  @media (max-width: 960px) {
    background-size: unset;
    height: unset;
    background-image: unset;
  }
}
</style>
