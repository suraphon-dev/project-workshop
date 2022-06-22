<template>
  <v-footer dark padless>
    <v-card flat tile class="card-footer" :class="[!breakpoint ? 'text-left' : 'text-center']">
      <v-row class="align-center my-6 mx-0">
        <v-col xl="4" lg="4" md="4" cols="12">
          <div class="padding-container height-300">
            <img src="~/assets/images/logo.png" width="65%" height="auto" />
            <div class="my-6">
              <h2>บริษัท ทุนภัทร จำกัด (มหาชน)</h2>
              <h4>{{ breakpoint }}ชั้น 9 อาคารสำนักงานเมืองไทย-ภัทร 1 252/6 ถนนรัชดาภิเษก แขวงห้วยขวาง กรุงเทพมหานคร 10310</h4>
            </div>
          </div>
        </v-col>
        <v-col xl="4" lg="4" md="4" cols="12">
          <v-row>
            <v-col v-for="i in 2" :key="i" cols="6">
              <div class="height-300">
                <div class="my-6">
                  <h1 class="font-24">เมนู</h1>
                </div>
                <div>
                  <h4 v-for="(item, index) in data.menu" :key="index" class="py-1">{{ item }}</h4>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-col>
        <v-col xl="4" lg="4" md="4" cols="12">
          <div class="height-300">
            <div class="my-6">
              <h1 class="font-24">ติดต่อเรา</h1>
            </div>
            <div v-for="(item, index) in data.contact" :key="index" class="py-1">
              <v-icon color="white" class="mx-2">{{ item.icon }}</v-icon>
              <span>{{ item.text }}</span>
            </div>
            <div class="my-12">
              <v-btn v-for="icon in icons" :key="icon" class="mx-2" elevation="0" fab dark large color="white">
                <v-icon color="#352c64" size="36"> {{ icon }} </v-icon>
              </v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
      <v-divider></v-divider>
      <v-row class="align-center ma-0">
        <v-col xl="6" lg="6" md="6" cols="12">
          <div class="d-flex justify-space-between padding-container">
            <div class="card-condition" :class="{ active: !breakpoint }">
              <span class="grey--text">แผนเว็บไซต์</span>
            </div>
            <div class="card-condition" :class="{ active: !breakpoint }">
              <span class="grey--text">ข้อตกลงและเงื่อนไข</span>
            </div>
            <div class="card-condition">
              <span class="grey--text">นโยบายข้อมูลส่วนตัว</span>
            </div>
          </div>
          <!-- <v-row class="padding-container">
            <v-col xl="2" lg="2" md="2" cols="12" class="card-condition" :class="{ active: !breakpoint }">
              <span class="grey--text">แผนเว็บไซต์</span>
            </v-col>
            <v-col xl="5" lg="5" md="5" cols="12" class="card-condition text-center" :class="{ active: !breakpoint }">
              <span class="grey--text px-6">ข้อตกลงและเงื่อนไข</span>
            </v-col>
            <v-col xl="5" lg="5" md="5" cols="12" class="card-condition">
              <span class="grey--text px-6">นโยบายข้อมูลส่วนตัว</span>
            </v-col>
          </v-row> -->
        </v-col>
        <v-col xl="6" lg="6" md="6" cols="12">
          <span class="grey--text">@2019 Phatra A© สงวนลิขสิทธิ์ 2562 บริษัทหลักทรัพย์จัดการกองทุน ภัทร จำกัดsset All rights reserved.</span>
        </v-col>
      </v-row>
    </v-card>
    <div class="white black--text pa-12" style="width: 100%">
      <v-row class="align-center">
        <v-col v-for="(item, index) in data.partner" :key="index" xl="3" lg="3" md="3" cols="6">
          <v-img contain :src="require(`assets/images/${item}`)" width="100%" />
        </v-col>
      </v-row>
    </div>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {
      icons: ['mdi-facebook', 'mdi-twitter', 'mdi-youtube'],
      data: {
        menu: ['รู้จัก บลจ.ภัทร', 'เกี่ยวกับเรา', 'ติดต่อเรา', 'คำถามที่พบบ่อย', 'สมัครงาน', 'Links'],
        contact: [
          {
            icon: 'mdi-phone-outline',
            text: '(66) 2305 9800'
          },
          {
            icon: 'mdi-printer',
            text: '(66) 2305 9803'
          },
          {
            icon: 'mdi-email-outline',
            text: 'customerservice@phatraasset.com'
          }
        ],
        partner: ['partner-logo-1.png', 'partner-logo-2.png', 'partner-logo-3.png', 'partner-logo-2.png']
      }
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
.card-footer {
  color: white;
  width: 100%;
  background-image: linear-gradient(to bottom, #6f6eb2 3%, #352c64 106%);
}

.height-300 {
  height: 300px;
}

.card-condition {
  padding: 0px 20px;
  // margin: 15px 0px;

  &.active {
    border-right: 1px solid gray;
  }
}
</style>
