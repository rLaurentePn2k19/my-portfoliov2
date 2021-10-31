<template>
  <v-app-bar app fixed color="background" flat height="100">
    <v-toolbar-title class="my_secondary--text font-weight-bold headline">
      <picture>
        <v-img width="95" src="/img/my-logo-1-removebg-preview.png"> </v-img>
      </picture>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-hover v-slot="{ hover }">
      <v-btn
        :text="!hover"
        :dark="hover"
        color="my_primary"
        class="button font-weight-bold text-capitalize"
      >
        About Me
      </v-btn>
    </v-hover>
    <v-hover v-slot="{ hover }">
      <v-btn
        :text="!hover"
        :dark="hover"
        class="mx-2 button font-weight-bold text-capitalize"
        color="my_primary"
      >
        Skills
      </v-btn>
    </v-hover>
    <v-hover v-slot="{ hover }">
      <v-btn
        :text="!hover"
        :dark="hover"
        color="my_primary"
        class="button font-weight-bold text-capitalize"
      >
        Projects
      </v-btn>
    </v-hover>
    <v-spacer></v-spacer>
    <v-btn
      color="my_primary"
      depressed
      class="
        rounded-lg
        pa-5
        text-capitalize
        shake
        white--text
        font-weight-black
      "
    >
      Contact Me
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "app-bar"
};
</script>

<style scoped>
.shake {
  animation: shake-animation 3s ease infinite;
  transform-origin: 50% 50%;
}
@keyframes shake-animation {
  0% {
    transform: translate(0, 0);
  }
  1.78571% {
    transform: translate(5px, 0);
  }
  3.57143% {
    transform: translate(0, 0);
  }
  5.35714% {
    transform: translate(5px, 0);
  }
  7.14286% {
    transform: translate(0, 0);
  }
  8.92857% {
    transform: translate(5px, 0);
  }
  10.71429% {
    transform: translate(0, 0);
  }
  100% {
    transform: translate(0, 0);
  }
}
</style>