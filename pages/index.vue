<template>
  <div>
    <the-slide-banner />
    <div class="background-content">
      <the-slide-subject />
      <panel-article-news />
    </div>
  </div>
</template>

<script>
import TheSlideSubject from '~/components/TheSlideSubject.vue'
import TheSlideBanner from '~/components/TheSlideBanner.vue'
import PanelArticleNews from '~/components/PanelArticleNews.vue'

export default {
  components: {
    TheSlideBanner,
    TheSlideSubject,
    PanelArticleNews
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
