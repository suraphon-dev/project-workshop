<template>
  <div>
    <div class="relative">
      <v-carousel cycle :height="650" hide-delimiter-background show-arrows-on-hover hide-delimiters dark>
        <div class="panel-header white--text">
          <v-row>
            <v-col xl="6" lg="6" md="6" cols="12">
              <div class="d-flex flex-column ma-16">
                <h4>โอกาศของคุณมาถึงแล้ว</h4>
                <h1>ลงทุนบริษัทชั้นนำของโลก</h1>
                <small>
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nisi porro earum omnis nam repellendus atque quisquam aliquam facere
                  dignissimos, inventore dolore, nesciunt,
                </small>
              </div>
            </v-col>
            <v-col xl="6" lg="6" md="6" cols="12">
              <div class="d-flex flex-column ma-16">
                <h1 class="text-uppercase">
                  phatra <br />
                  gnp
                </h1>
                <hr />
                <h4 class="my-2">
                  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ducimus quo dolore, nesciunt corporis soluta vitae culpa tenetur ipsam
                  odit. Natus.
                </h4>
                <h4 class="">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Aspernatur, eveniet!</h4>
              </div>
            </v-col>
          </v-row>
        </div>
        <v-carousel-item v-for="(item, i) in banner" :key="i">
          <img :src="item.src" class="image-banner" alt="image-banner" />
        </v-carousel-item>
      </v-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      banner: [
        {
          src: 'https://images.unsplash.com/photo-1541746972996-4e0b0f43e02a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1522071820081-009f0129c71c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.image-banner {
  width: 100%;
  height: 625px;
  object-fit: cover;
  @media (max-width: 600px) {
    height: 750px;
  }
}

.relative {
  position: relative;
}
.panel-header {
  width: 100%;
  height: auto;
  position: absolute;
  top: 0;
  z-index: 99;
}
</style>
