<template>
  <v-sheet class="mx-auto d-flex justify-center" max-width="2000">
    <v-slide-group v-model="model" class="pa-4" center-active show-arrows>
      <v-slide-item v-for="n in 15" :key="n" v-slot="{ active, toggle }">
        <div class="panel-subject ma-4" :class="{ 'class-active': active }" @click="toggle">
          <h4 :class="active ? 'white--text' : 'black--text'">Title</h4>
        </div>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
</template>

<script>
export default {
  data() {
    return {
      model: null
    }
  }
}
</script>

<style lang="scss" scoped>
.panel-subject {
  height: 125px;
  width: 220px;
  border-bottom: 7px solid #64599e;
  background-image: linear-gradient(to right, #eeedf2 3%, #ebeaef 34%, #e5e5e8 94%);
  border-radius: 5px;
  display: flex;
  align-items: center;
  justify-items: center;
  justify-content: center;

  &.class-active {
    background-image: linear-gradient(to left, #655a9f, #8b8bc1);
  }
}
</style>
