<template>
  <v-app-bar app fixed color="background" flat height="100">
    <v-toolbar-title class="my_secondary--text font-weight-bold headline">
      <picture>
        <v-img class="logo" @click="goHome" width="95" src="/img/my-logo-1-removebg-preview.png"> </v-img>
      </picture>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-hover v-slot="{ hover }">
        <v-btn
          :text="!hover"
          :dark="hover"
          color="my_primary"
          class="button font-weight-bold text-capitalize"
          @click="goToAboutMe"
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
        @click="goToSkills"
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
        @click="goToProjects"
      >
        Portfolio
      </v-btn>
    </v-hover>
    <v-spacer></v-spacer>
    <v-btn
      color="my_primary"
      depressed
      class="rounded-lg pa-5 text-capitalize white--text font-weight-black"
      @click="goToContact"
    >
      Contact Me
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "app-bar",

  methods: {
    goToAboutMe() {
      this.$vuetify.goTo('#about-me', {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    },

    goToSkills() {
      this.$vuetify.goTo('#skills', {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    },

    goToProjects() {
      this.$vuetify.goTo('#projects', {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    },

    goToContact(){
      this.$vuetify.goTo('#contact', {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    },

    goHome(){
      this.$vuetify.goTo('#home', {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    }
  }
};
</script>

<style scoped>

.logo{
  cursor: pointer;
}

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