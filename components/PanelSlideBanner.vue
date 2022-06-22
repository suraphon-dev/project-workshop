<template>
  <div class="relative">
    <v-carousel v-model="model" height="950" cycle hide-delimiter-background show-arrows-on-hover hide-delimiters dark>
      <v-carousel-item v-for="(item, i) in banner" :key="i">
        <div class="panel-header white--text">
          <v-row>
            <v-col xl="6" lg="6" md="6" cols="12">
              <div class="d-flex flex-column ma-16">
                <h4 class="grey--text font-24">โอกาสที่คุณจะได้</h4>
                <h1 class="">ลงทุนในบริษัทชั้นนำของโลก</h1>
                <div :class="{ 'text-worning': !breakpoint }">
                  <small class="font-8 grey--text">
                    คำเตือน : ผู้ลงทุนควรทำความเข้าใจลักษณะสินค้า
                    เงื่อนไขผลตอบแทนและความเสี่ยงก่อนตัดสินใจลงทุนและควรศึกษาข้อมูลเพิ่มเติมในหนังสือชี้ชวน ผลการดำเนินงาน ในอดีตของกองทุนรวม
                    มิได้เป็นสิ่งยืนยันถึงผลการดำเนินงานในอนาคต เนื่องจากกองทุนป้องกันความเสี่ยงจากอัตราแลกเปลี่ยนตามดุลยพินิตของผู้จัดการกองทุน
                    ดังนั้นผู้ลงทุนอาจจะขาดทุนหรือได้รับผลกำไรจากอัตราแลกเปลี่ยน/หรือได้รับเงินคืนต่ำกว่าเงินลงทุนเริ่มแรกได้
                    กองทุนหลักจะนำเงินไปลงทุนในหุ้นสามัธทั่วโลก ในหลายสกุลเงินตามแต่ละประเทศที่กองทุนหลักไปลงทุน
                    โดยกองทุนหลักอาจเข้าทำสัญญาซื้อขายล่วงหน้าเพื่อป้องกันความเสี่ยง จากอัตราแลกเปลี่ยนตามดุลยพินิต ของผู้จัดการลงทุน
                  </small>
                </div>
              </div>
            </v-col>
            <v-col xl="6" lg="6" md="6" cols="12">
              <div class="d-flex flex-column ma-16">
                <h1 class="text-uppercase text-logo">
                  phatra <br />
                  gnp
                </h1>
                <hr />
                <h4 class="my-4 grey--text font-20">
                  กองทุนที่คัดสรรการลงทุนที่หลากหลายจากบริษัทชั้นนำของโลก โดยทีมนักวิเคราะห์และผู้จัดการกองทุนจาก Capital Group
                  ที่มีประสบการณ์การลงทุนกว่า 80 ปี
                </h4>
                <h4 class="font-20">อีกระดับแห่งการลงทุน</h4>
              </div>
            </v-col>
          </v-row>
        </div>
        <v-parallax height="950" :src="item.src" />
      </v-carousel-item>
    </v-carousel>
    <panel-slide-subject />
  </div>
</template>

<script>
import PanelSlideSubject from './PanelSlideSubject.vue'

export default {
  components: { PanelSlideSubject },

  data() {
    return {
      model: 0,
      banner: [
        {
          src: 'https://images.unsplash.com/photo-1639322537228-f710d846310a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1632&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1639322537231-2f206e06af84?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1632&q=80'
        }
      ]
    }
  },

  computed: {
    breakpoint() {
      return this.$vuetify.breakpoint.smAndDown
    }
  }
}
</script>

<style lang="scss" scoped>
.parallax {
  height: 850px;
  @media (max-width: 960px) {
    height: 1200px;
  }
}

.panel-header {
  width: 100%;
  height: auto;
  position: absolute;
  top: 0;
  z-index: 99;
}

.text-worning {
  height: 550px;
  display: flex;
  align-items: flex-end;
}
</style>
