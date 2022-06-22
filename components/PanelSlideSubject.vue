<template>
  <div>
    <v-sheet class="mx-auto d-flex justify-center" max-width="2000">
      <v-slide-group v-model="model" class="padding-container postion-subject" center-active show-arrows>
        <v-slide-item v-for="(item, index) in item" :key="index" v-slot="{ active, toggle }">
          <div class="panel-subject ma-4" :class="{ 'class-active': active }" @click="toggle">
            <h4 :class="active ? 'white--text' : 'black--text'">{{ item }}</h4>
          </div>
        </v-slide-item>
      </v-slide-group>
    </v-sheet>
  </div>
</template>

<script>
export default {
  data() {
    return {
      model: null,
      item: [
        'Abou Us',
        'Awards',
        'Our Businesses',
        'News&Activites',
        'Abou Us',
        'Awards',
        'Our Businesses',
        'News&Activites',
        'Abou Us',
        'Awards',
        'Our Businesses',
        'News&Activites'
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.panel-subject {
  height: 95px;
  width: 260px;
  border-bottom: 7px solid #64599e;
  background-image: linear-gradient(to right, #eeedf2 3%, #ebeaef 34%, #e5e5e8 94%);
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-items: center;
  justify-content: center;
  @media (max-width: 960px) {
    height: 125px;
    width: 220px;
  }
  &.class-active {
    background-image: linear-gradient(to left, #655a9f, #8b8bc1);
  }
}
.postion-subject {
  position: absolute;
  bottom: -55px;

  @media (max-width: 960px) {
    bottom: -125px;
  }
}
</style>
