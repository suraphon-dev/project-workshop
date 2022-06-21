<template>
  <v-container class="my-6">
    <v-carousel :show-arrows="false" hide-delimiter-background show-arrows-on-hover>
      <template v-for="(item, index) in slide">
        <v-carousel-item v-if="(index + 1) % columns === 1 || columns === 1" :key="index">
          <v-row>
            <template v-for="(n, i) in columns">
              <template v-if="+index + i < slide.length">
                <v-col xl="4" lg="4" md="4" cols="12" :key="i">
                  <div v-if="+index + i < slide.length" :color="slide[+index + i]">
                    <img :src="slide[+index + i].image" width="100%" height="210px" alt="" />
                    <div class="my-6">
                      <h2>{{ slide[+index + i].title }}</h2>
                    </div>
                  </div>
                </v-col>
              </template>
            </template>
          </v-row>
        </v-carousel-item>
      </template>
    </v-carousel>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      slide: [
        {
          title: 'KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม',
          image: require('@/assets/images/content-1.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'KKP Focus ช่วงที่ 1 ย่อประเด็นโลก โยกประเด็นร้อน ',
          image: require('@/assets/images/content-2.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม',
          image: require('@/assets/images/content-3.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม',
          image: require('@/assets/images/content-1.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'KKP Focus ช่วงที่ 1 ย่อประเด็นโลก โยกประเด็นร้อน ',
          image: require('@/assets/images/content-2.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        },
        {
          title: 'KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม',
          image: require('@/assets/images/content-3.jpg'),
          content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sequi, asperiores!'
        }
      ]
    }
  },
  computed: {
    columns() {
      if (this.$vuetify.breakpoint.xl) {
        return 3
      }

      if (this.$vuetify.breakpoint.lg) {
        return 3
      }

      if (this.$vuetify.breakpoint.md) {
        return 2
      }

      return 1
    }
  }
}
</script>

<style lang="scss">
.theme--dark.v-btn.v-btn--icon {
  color: #626099;
}
</style>
