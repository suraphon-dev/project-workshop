<template>
  <v-container>
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
      </v-col>
    </v-row>
  </v-container>
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
  }
}
</script>

<style lang="scss" scoped></style>
