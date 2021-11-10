<template>
  <v-container fluid fill-height class="my-16">
    <v-row>
      <v-col cols="12" md="6" class="d-flex align-center justify-center">
        <div class="display-4 white--text">
          <div class="headline mx-2">Hello</div>
          I'm Rangie
          <div class="display-1 white--text mx-2">Freelance Web Developer</div>
          <div class="white--text d-flex align-start ma-2 mt-10">
            <v-hover v-slot="{ hover }">
              <v-btn
                :outlined="hover"
                width="50%"
                height="70"
                class="
                  text-capitalize
                  title
                  rounded-lg
                  white--text
                  font-weight-black
                "
                color="my_primary"
                depressed
                @click="goToContact"
              >
                Hire Me
              </v-btn>
            </v-hover>
          </div>
        </div>
      </v-col>
      <v-col cols="12" md="6" class="d-flex justify-center my-img">
        <div class="d-flex justify-center">
          <picture>
            <v-img
              width="500"
              src="/img/IMG20211109115359-removebg-preview.png"
              lazy-src="/img/IMG20211109115359-removebg-preview.png"
              alt="programmer"
              contain
              class="my-back-img"
            />
          </picture>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "home",
  methods: {
    goToContact(){
      this.$vuetify.goTo('#contact', {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    }
  }
};
</script>

<style scoped>
.floating-img {
  float: left;
}
.my-img {
  background-image: url("/img/blob-haikei-1.svg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position-x: -3rem;
}

.my-back-img {
  animation: pulse 3s ease-out infinite alternate;
  transform-origin: 50% 50%;
  margin-top: -100px;
}

@keyframes pulse {
  0% {
    transform: translateY(0);
  }

  5% {
    transform: translateY(-10px);
  }

  10% {
    transform: translateY(0);
  }

  15% {
    transform: translateY(-10px);
  }

  20% {
    transform: translateY(0);
  }

  100% {
    transform: translateY(0);
  }
}
</style>