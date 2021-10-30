<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <div>
          <v-slide-group
            v-model="model"
            active-class="success"
            show-arrows
            center-active
          >
            <v-slide-item v-for="n in 3" :key="n" v-slot="{ active, toggle }">
              <v-card
                :color="active ? 'my_primary' : 'transparent'"
                class="ma-4 pa-2 rounded-xl"
                height="500"
                width="350"
                @mouseenter="toggle"
                :flat="!active"
                :elevation="active ? '24' : '0'"
              >
                <v-card-title class="d-flex justify-center white--text mt-2">
                  <div class="display-1 font-weight-light">Project Name</div>
                </v-card-title>
                <v-card-text class="white--text px-4">
                  <v-row>
                    <v-col cols="12" class="d-flex justify-center">
                      <div class="title font-weight-light text-center">
                        <blockquote>
                          Lorem ipsum dolor sit amet, consectetur adipisicing
                          elit. Dolore distinctio perspiciatis voluptatem id?
                          Fugit in labore voluptate vitae impedit nesciunt
                          provident adipisci non quos quae! Fugit aliquid dolore
                          facilis culpa.
                        </blockquote>
                      </div>
                    </v-col>
                  </v-row>
                </v-card-text>
                <v-card-actions class="d-flex justify-center">
                  <v-btn
                    v-if="active"
                    :color="active ? 'background' : 'my_primary'"
                    dark
                    width="70%"
                    class="rounded-xl btn text-capitalize"
                    height="65"
                  >
                    <v-icon size="30"> mdi-github </v-icon>
                    <span class="subtitle-1 mx-2"> Github </span>
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-slide-item>
          </v-slide-group>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "temp2",
  data: () => ({
    model: null
  })
};
</script>

<style scoped>
.btn {
  position: absolute;
  bottom: 2rem;
}
</style>