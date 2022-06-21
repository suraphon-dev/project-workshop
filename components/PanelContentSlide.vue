<template>
  <v-container class="my-6">
    <vueper-slides
      arrows-outside
      bullets-outside
      fixed-height="475px"
      class="no-shadow"
      :arrows="false"
      autoplay
      :visible-slides="3"
      slide-multiple
      :gap="3"
      :dragging-distance="200"
      :breakpoints="{ 800: { visibleSlides: 1, slideMultiple: 1 } }"
      slide-content-outside="top"
    >
      <vueper-slide v-for="(item, index) in slide" :key="index" :image="item.image" class="pa-4" title="test" />
    </vueper-slides>
  </v-container>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'
export default {
  components: {
    VueperSlides,
    VueperSlide
  },

  data() {
    return {
      slide: [],
      slide: [
        {
          title: 'test1',
          image: require('@/assets/images/article-1.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'test2',
          image: require('@/assets/images/article-2.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'test3',
          image: require('@/assets/images/article-3.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'test4',
          image: require('@/assets/images/article-1.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'test5',
          image: require('@/assets/images/article-2.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'test6',
          image: require('@/assets/images/article-3.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>
