<template>
  <div>
    <!-- <v-navigation-drawer v-model="drawer" dark>
     
    </v-navigation-drawer> -->

    <v-app-bar app dark>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data: () => ({ drawer: null })
}
</script>
