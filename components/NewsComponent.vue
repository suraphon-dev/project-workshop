<template>
  <div>
    <vueper-slides 3d fixed-height="350px" :arrows="false" arrows-outside bullets-outside :dragging-distance="50" autoplay>
      <vueper-slide v-for="(item, index) in slide" :key="index" :image="item.image" :title="item.title" :content="item.content" />
    </vueper-slides>
  </div>
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
      slide: [
        {
          title: '',
          image: require('@/assets/images/article-1.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: '',
          image: require('@/assets/images/article-2.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: '',
          image: require('@/assets/images/article-3.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
.vueperslide__content-wrapper:not(.vueperslide__content-wrapper--outside-top):not(.vueperslide__content-wrapper--outside-bottom) {
  text-align: left !important;
  justify-content: end !important;
  padding: 20px !important;
  color: white;
  font-weight: bold;
  font-size: 24px;
}

.vueperslides__bullet .default {
  background-color: rgba(255, 253, 253, 0.3);
  border: 1px solid #adadb9;
  box-shadow: none;
  transition: 0.3s;
  width: 16px;
  height: 16px;
}

.vueperslides__bullet--active .default {
  background-color: #594f74;
}

.vueperslides__bullet span {
  display: block;
  color: #fff;
  font-size: 10px;
  opacity: 0.8;
}
</style>
