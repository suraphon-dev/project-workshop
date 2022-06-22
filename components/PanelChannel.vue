<template>
  <div class="padding-container">
    <v-row class="align-center mb-12">
      <v-col xl="4" lg="4" md="4" cols="12" style="padding-left: 50px">
        <v-row class="align-center">
          <div class="line-title"></div>
          <h1 style="padding: 0px 60px" class="color-theme" data-aos="fade-down">KKP Channel</h1>
        </v-row>
      </v-col>
      <v-col xl="8" lg="8" md="8" cols="12" class="mx-0 px-0">
        <span class="grey--text" data-aos="fade-down">
          อัปเดตทุกความรู้ด้านการเงินและการลงทุนก่อนใคร พร้อมอินเทรนด์ไปกับหลากหลายเรื่องราวไลฟ์สไตล์
        </span>
      </v-col>
    </v-row>
    <div class="px-12">
      <v-tabs v-model="tab" slider-color="grey" color="basil" background-color="white" light show-arrows>
        <v-tab v-for="item in items" :key="item.tab">
          {{ item.tab }}
        </v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <v-tab-item v-for="(item, index) in items" :key="index">
          <v-row class="my-6 align-center">
            <v-col xl="8" lg="8" md="8" cols="12">
              <video-player-component v-if="tab == index" />
            </v-col>
            <v-col xl="4" lg="4" md="4" cols="12" class="my-6">
              <div class="line-textcontent">
                <h1 class="my-2 color-theme">{{ item.tab }}</h1>
                <span class="grey--text">{{ item.content }}</span>
              </div>
            </v-col>
          </v-row>
        </v-tab-item>
      </v-tabs-items>
    </div>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
import VideoPlayerComponent from './VideoPlayerComponent.vue'
export default {
  components: { VideoPlayerComponent },
  mixins: [aosMixin],

  data() {
    return {
      tab: null,
      items: [
        {
          tab: 'KKP FOCUS',
          content: 'ฝนนักสู้ พบเรื่องราวจริง เจ็บจริง ประสบความสำเร็จจริง ที่จะเป็นแรงกระตุ้นให้ SME นักสู้รุ่นต่อไป ได้ก้าวไปถึงฝัน'
        },
        { tab: 'OPTIMISE', content: 'Tab 2 Content' },
        { tab: 'KKP Advisor', content: 'Tab 3 Content' },
        { tab: 'Other', content: 'Tab 4 Content' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.line-title {
  transform: rotate(90deg);
  border: 1px solid #84848f;
  height: 65px;
}

.line-textcontent {
  border-style: solid;
  border-width: 3px;
  -o-border-image: linear-gradient(to right, #d0cfd8 -3%, #e9eaef -55%, #b9b9c3 111%) 100% 0 100% 0/3px 0 3px 0;
  border-image: linear-gradient(to right, #d0cfd8 -3%, #e9eaef -55%, #b9b9c3 111%) 100% 0 100% 0/3px 0 3px 0;
  line-height: 50px;
  background-color: #ffffff;
  color: black;
  padding: 50px 0px;
}
</style>
