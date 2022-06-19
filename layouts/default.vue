<template>
  <div>
    <v-app id="inspire">
      <layout-navbar />
      <v-main>
        <Nuxt />
      </v-main>
      <layout-footer />
    </v-app>
  </div>
</template>

<script>
import LayoutNavbar from '~/components/layout/LayoutNavbar.vue'
import LayoutFooter from '~/components/layout/LayoutFooter.vue'
export default {
  components: {
    LayoutNavbar,
    LayoutFooter
  }
}
</script>
