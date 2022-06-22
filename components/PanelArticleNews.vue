<template>
  <div class="padding-container">
    <v-row>
      <v-col xl="8" lg="8" md="8" cols="12">
        <div>
          <panel-header title="Article" />
          <article-component />
        </div>
      </v-col>
      <v-col xl="4" lg="4" md="4" cols="12">
        <div>
          <panel-header title="News" />
          <news-component />
        </div>
        <div class="panel-setprice">
          <h2 class="text-title color-theme">Set Index</h2>
          <div>
            <v-img :src="imageSetIndex" width="95%" height="auto" class="img-price" />
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import PanelHeader from '~/components/ui/PanelHeader.vue'
import ArticleComponent from './ArticleComponent.vue'
import NewsComponent from './NewsComponent.vue'

export default {
  components: {
    PanelHeader,
    ArticleComponent,
    NewsComponent
  },

  data() {
    return {
      imageSetIndex: require('@/assets/images/setindex.jpg')
    }
  }
}
</script>

<style lang="scss" scoped>
.panel-setprice {
  background-color: white;
  height: auto;
  padding: 15px 0px;

  & .text-title {
    padding: 15px 20px 0px 20px;
  }

  & .img-price {
    margin: 15px;
  }
}
</style>
