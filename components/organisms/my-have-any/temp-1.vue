<template>
  <v-container fluid fill-height :style="[backgroundWaveStyle]">
    <v-row class="mx-16 px-16 mt-6">
      <v-col cols="12" class="d-flex justify-center mb-6">
        <div class="white--text display-3">Have Any Project In Mind?</div>
      </v-col>
      <v-col cols="12" class="d-flex justify-center">
        <v-hover v-slot="{ hover }">
          <v-btn
            :outlined="hover"
            color="background"
            :class="`${hover ? 'white--text' : 'my_primary--text'} text-capitalize headline font-weight-bold rounded-lg`"
            width="20%"
            height="70"
          >
            Hire Me
          </v-btn>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "anyProject",
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
