<template>
  <v-container fill-height class="my-16">
    <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <div class="white--text display-3">
          <div class="mb-4">What I do</div>
          <v-divider
            v-for="i in 5"
            :key="i"
            class="mx-12 my_primary"
          ></v-divider>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex justify-center">
        <blockquote class="white--text headline text-center">
          Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
          officia deserunt mollit anim id est laborum. Sed ut perspiciatis unde
          omnis iste natur
        </blockquote>
      </v-col>
    </v-row>
    <v-row class="mt-10">
      <v-col cols="12" md="6" v-for="i in 2" :key="i">
        <v-lazy
          v-model="isActive"
          :options="{
            threshold: 1.0,
          }"
          min-height="200"
          :transition="`scroll-y-transition`"
        >
          <v-card
            height="300"
            :color="i > 1 ? '#f9be35' : '#3db7fc'"
            flat
            class="rounded-lg px-16 pt-12"
          >
            <div class="mx-4">
              <picture>
                <v-img
                  width="80"
                  src="/img/web-dev.png"
                  lazy-src="/img/web-dev.png"
                >
                </v-img>
              </picture>
            </div>
            <v-card-title class="display-1 white--text font-weight-bold">
              <div>Web Development</div>
            </v-card-title>
            <v-card-text class="white--text subtitle-1 font-weight-bold">
              <blockquote>
                Duis aute irure dolor in reprehenderit in voluptate velit esse
                cillum dolore eu fugiat
              </blockquote>
            </v-card-text>
          </v-card>
        </v-lazy>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "skills",
  data() {
    return {
      isActive: false
    };
  }
};
</script>

