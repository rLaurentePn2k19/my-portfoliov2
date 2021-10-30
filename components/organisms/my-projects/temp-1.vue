<template>
  <v-container fluid fill-height :style="[backgroundWaveStyle]">
    <v-row class="mx-16 px-16">
      <v-col cols="12" class="d-flex justify-center mb-2">
        <div class="white--text display-3">Projects</div>
      </v-col>
      <v-col cols="12" md="4" v-for="i in 3" :key="i">
        <v-card
          flat
          color="background"
          width="100%"
          height="250"
          class="rounded-xl py-16"
        >
            <v-card-title class="my_secondary--text d-flex justify-center font-weight-light headline">
                Project Title
            </v-card-title>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "about",
  data() {
    return {
      backgroundWaveStyle: {
        "background-image": `url(${"/img/wave-3.svg"})`,
        "background-position": "center",
        "background-repeat": "no-repeat",
        "background-size": "cover",
        height: "100vh"
      }
    };
  }
};
</script>
