<template>
  <div>
    <v-navigation-drawer v-model="drawer" fixed temporary style="z-index: 999" width="340" dark>
      <div>
        <v-col xl="6" lg="6" md="6" cols="12" class="d-flex align-center ma-4">
          <v-app-bar-nav-icon @click="drawer = !drawer" color="white"></v-app-bar-nav-icon>
          <img class="mx-6" src="~/assets/images/logo.png" width="250px" height="50px" />
        </v-col>
      </div>
      <div>
        <v-list dense>
          <v-subheader class="mx-3">Menu</v-subheader>
          <v-list-item-group v-model="selectedItem">
            <v-list-item v-for="(item, i) in items" :key="i" class="my-1">
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </div>
    </v-navigation-drawer>
    <v-app-bar class="black" :height="setBarHeight">
      <v-row class="align-center">
        <v-col xl="6" lg="6" md="6" cols="12" class="d-flex align-center">
          <v-app-bar-nav-icon @click="drawer = !drawer" color="white"></v-app-bar-nav-icon>
          <img class="mx-6" src="~/assets/images/logo.png" width="250px" height="50px" />
        </v-col>
        <v-col xl="6" lg="6" md="6" cols="12">
          <v-row no-gutters>
            <v-col xl="10" lg="10" md="10" cols="8">
              <v-text-field class="custom" color="grey darken" :loading="loading" @focus="focusSearch" @blur="focusSearchCancel">
                <v-icon slot="append" color="white"> mdi-magnify </v-icon>
              </v-text-field>
            </v-col>
            <v-col xl="2" lg="2" md="2" cols="4" class="px-8">
              <v-select v-model="language" class="custom" :items="['TH', 'EN']" />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
      language: 'TH',
      loading: false,
      selectedItem: 1,
      items: [
        { text: 'หน้าแรก', icon: 'mdi-home' },
        { text: 'รู้จัก บลจ.ภัทร', icon: 'mdi-domain' },
        { text: 'เกี่ยวกับเรา', icon: 'mdi-contacts-outline' },
        { text: 'ติดต่อเรา', icon: 'mdi-phone-outline' },
        { text: 'คำถามที่พบบ่อย', icon: 'mdi-bullhorn' },
        { text: 'สมัครงาน', icon: 'mdi-account-plus' },
        { text: 'Links', icon: 'mdi-linkedin' }
      ]
    }
  },

  computed: {
    breakpoint() {
      return this.$vuetify.breakpoint.smAndDown
    },

    setBarHeight() {
      return this.breakpoint ? '200' : '120'
    }
  },

  methods: {
    focusSearch() {
      this.loading = true
    },

    focusSearchCancel() {
      this.loading = false
    }
  }
}
</script>
