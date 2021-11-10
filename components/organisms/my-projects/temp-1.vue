<template>
  <div class="project-container">
    <v-container fill-height class="my-16 py-16">
      <v-row>
        <v-col cols="12" class="d-flex justify-center">
          <div class="display-3 white--text">
            <div class="mb-4">My Portfolio</div>
            <v-divider
              v-for="i in 5"
              :key="i"
              class="mx-16 my_primary"
            ></v-divider>
          </div>
        </v-col>
      </v-row>
      <v-row class="mt-6">
        <v-col cols="12">
          <v-container fluid class="img-cont">
            <v-row class="mb-6">
              <v-col cols="7">
                <v-card class="rounded-0" :height="500" width="100%">
                  <v-img
                    height="100%"
                    src="/img/laptop-dark.jpg"
                    lazy-src="/img/laptop-dark.jpg"
                  >
                  </v-img>
                </v-card>
                <v-row class="mt-2">
                  <v-col cols="6">
                    <v-card class="rounded-0" :height="274" width="100%">
                      <v-img
                        height="100%"
                        src="/img/my-wallpapper.png"
                        lazy-src="/img/my-wallpapper.png"
                      >
                      </v-img>
                    </v-card>
                  </v-col>
                  <v-col cols="6">
                    <v-card class="rounded-0" :height="274" width="100%">
                      <v-img
                        src="/img/rangie-removebg.png"
                        lazy-src="/img/rangie-removebg.png"
                        height="100%"
                      />
                    </v-card>
                  </v-col>
                </v-row>
              </v-col>
              <v-col cols="5">
                <v-card class="rounded-0" :height="225" width="100%">
                  <v-img
                    src="/img/vue.png"
                    lazy-src="/img/vue.png"
                    height="100%"
                  />
                </v-card>
                <v-row class="mt-2">
                  <v-col cols="12">
                    <v-card class="rounded-0" :height="300" width="100%">
                      <v-img
                        height="100%"
                        src="/img/ruins.jpg"
                        lazy-src="/img/ruins.jpg"
                      ></v-img>
                    </v-card>
                  </v-col>
                  <v-col cols="12">
                    <v-card class="rounded-0" :height="225" width="100%">
                      <v-img
                        src="/img/pn.jpg"
                        lazy-src="/img/pn.jpg"
                        height="100%"
                      />
                    </v-card>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "projects",
  data() {
    return {
      images: [
        {
          title: "image 1",
          url:
            "https://img00.deviantart.net/e895/i/2017/275/7/d/ultra_sun_ultra_moon_by_kawacy-dbpbuiq.jpg"
        },
        {
          title: "image 2",
          url:
            "https://img00.deviantart.net/870d/i/2009/174/d/b/sweet_summer_ii_by_zanasoul.jpg"
        },
        {
          title: "image 3",
          url:
            "https://pre00.deviantart.net/9b5b/th/pre/i/2017/205/c/8/electra_by_mistanphotography-dbhgxsz.jpg"
        },
        {
          title: "image 4",
          url:
            "https://img00.deviantart.net/47b3/i/2017/140/0/7/wonder_woman_by_pencilhead7-db9w9lw.png"
        },
        {
          title: "image 5",
          url:
            "https://orig00.deviantart.net/2b7a/f/2017/275/5/6/daily_paint_1777__swineapple_by_cryptid_creations-dbpboas.png"
        },
        {
          title: "image 6",
          url:
            "https://pre00.deviantart.net/a41c/th/pre/i/2015/014/9/8/swan_by_avine-d8dw53d.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
.project-container {
  background-color: #2b2c2c;
}
.img-cont {
  background-color: #2b2c2c;
}
</style>