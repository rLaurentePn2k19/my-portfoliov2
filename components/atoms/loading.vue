<template>
  <div class="loader">
    <v-row align="center">
      <v-col cols="12">
        <v-card class="mx-auto pa-10" color="transparent" flat>
          <v-row>
            <v-col cols="12" class="d-flex justify-center">
              <div class="zoom-in-out">
                <picture>
                  <v-img width="400" src="/img/my-logo-1-removebg-preview.png" lazy-src="/img/my-logo-1-removebg-preview.png">
                  </v-img>
                </picture>
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "loading"
};
</script>

<style scoped>
.loader {
  margin-top: 20rem;
}
.zoom-in-out {
  margin: 2rem;
  width: 7rem;
  height: 7rem;
  animation: zoom-in-zoom-out 1s ease infinite;
}

@keyframes zoom-in-zoom-out {
  0% {
    transform: scale(1, 1);
  }
  50% {
    transform: scale(1.5, 1.5);
  }
  100% {
    transform: scale(1, 1);
  }
}
</style>