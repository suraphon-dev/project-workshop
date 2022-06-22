<template>
  <v-row class="my-2">
    <v-col xl="7" lg="7" md="7" cols="12">
      <v-img width="auto" height="auto" :src="imageArticle1" />
    </v-col>
    <v-col xl="5" lg="5" md="5" cols="12">
      <div>
        <h2 class="my-2 color-theme font-24 font-weight-bold text-overflow colum2">
          Margin of Safety กลยุทธ์การลงทุนอย่างปลอดภัย หลักการลงทุนของเบนจามิน เกรแฮม
        </h2>
        <span class="font-16 grey--text font-weight-bold text-overflow colum8">
          ตอบคำถามที่ว่า คุณมีความจำเป็น พร้อมเป็นเจ้าของหรือยัง เช่น เพื่อหน้าที่การงาน อาชีพ หรือการเดินทาง ความสะดวกสบาย
          เพราะการซื้อรถนอกจากค่ารถแล้ว ยังมีค่าน้ำมัน ค่าบำรุงรักษา ค่าประกันภัย ซึ่งเป็นค่าใช้จ่ายในระยะยาว ตอบคำถามที่ว่า คุณมีความจำเป็น
          พร้อมเป็นเจ้าของหรือยัง เช่น เพื่อหน้าที่การงาน อาชีพ หรือการเดินทาง ความสะดวกสบาย เพราะการซื้อรถนอกจากค่ารถแล้ว ยังมีค่าน้ำมัน
          ค่าบำรุงรักษา ค่าประกันภัย ซึ่งเป็นค่าใช้จ่ายในระยะยาว ตอบคำถามที่ว่า คุณมีความจำเป็น พร้อมเป็นเจ้าของหรือยัง เช่น เพื่อหน้าที่การงาน อาชีพ
          หรือการเดินทาง ความสะดวกสบาย เพราะการซื้อรถนอกจากค่ารถแล้ว ยังมีค่าน้ำมัน ค่าบำรุงรักษา ค่าประกันภัย ซึ่งเป็นค่าใช้จ่ายในระยะยาว
        </span>
        <panel-tags text="การลงทุน" />
      </div>
    </v-col>
    <v-col xl="6" lg="6" md="6" cols="12">
      <v-img width="auto" height="auto" :src="imageArticle2" />
      <h2 class="mt-5 color-theme font-24 font-weight-bold text-overflow colum3">จับจังหวะการลงทุนเป็นก็สร้างเงินล้านได้ง่ายๆใกล้แค่เอื้อม</h2>
      <panel-tags text="การลงทุน" />
    </v-col>
    <v-col xl="6" lg="6" md="6" cols="12">
      <v-img width="auto" height="auto" :src="imageArticle3" />
      <h2 class="mt-5 color-theme font-24 font-weight-bold text-overflow colum3">Margin of Safety กลยุทธ์การลงทุนอย่างปลอดภัย Margin of Safety</h2>
      <panel-tags text="การลงทุน" />
    </v-col>
  </v-row>
</template>

<script>
import ImageArticle1 from '~/assets/images/article-1.jpg'
import ImageArticle2 from '~/assets/images/article-2.jpg'
import ImageArticle3 from '~/assets/images/article-3.jpg'
import PanelTags from './ui/PanelTags.vue'
export default {
  components: { PanelTags },

  data() {
    return {
      imageArticle1: ImageArticle1,
      imageArticle2: ImageArticle2,
      imageArticle3: ImageArticle3
    }
  }
}
</script>
