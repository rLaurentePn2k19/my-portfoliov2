<template>
  <div class="project-container">
    <v-container fill-height class="my-16 py-16">
      <v-row>
        <v-col cols="12" class="d-flex justify-center">
          <div class="display-3 white--text">
            <div class="mb-4">Latest Works</div>
            <v-divider
              v-for="i in 5"
              :key="i"
              class="mx-16 my_primary"
            ></v-divider>
          </div>
        </v-col>
        <v-col cols="12" class="d-flex justify-center">
          <div class="headline white--text text-center">
            <blockquote>
              Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
              officia deserunt mollit anim id est laborum. Sed ut perspiciatis
              unde omnis iste natus
            </blockquote>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-tabs right background-color="transparent" color="my_primary" >
            <v-tab class="white--text">Landscape</v-tab>
            <v-tab class="white--text">City</v-tab>
            <v-tab class="white--text">Abstract</v-tab>

            <v-tab-item v-for="n in 3" :key="n">
              <v-container fluid class="img-cont">
                <v-row>
                  <v-col v-for="i in 6" :key="i" cols="12" md="4">
                    <v-img
                      :src="`https://picsum.photos/500/300?image=${
                        i * n * 5 + 10
                      }`"
                      :lazy-src="`https://picsum.photos/10/6?image=${
                        i * n * 5 + 10
                      }`"
                      aspect-ratio="1.5"
                    ></v-img>
                  </v-col>
                </v-row>
              </v-container>
            </v-tab-item>
          </v-tabs>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "projects"
};
</script>

<style scoped>
.project-container {
  background-color: #2b2c2c;
}
.img-cont{
  background-color: #2b2c2c;
}
</style>