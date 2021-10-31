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
                <v-btn :outlined="hover" width="50%" height="70" class="text-capitalize title rounded-lg white--text font-weight-black" color="my_primary" depressed>
                    Hire Me
                </v-btn>
            </v-hover>
          </div>
        </div>
      </v-col>
      <v-col cols="12" md="6" class="d-flex justify-start my-img">
        <div class="d-flex justify-center">
          <picture>
            <v-img
              width="500"
              src="/img/steve.png"
              lazy-src="/img/steve.png"
              alt="programmer"
              contain
            />
          </picture>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "home"
};
</script>

<style scoped>
.floating-img {
  float: left;
}
.my-img{
    background-image: url('/img/blob-haikei-1.svg');
    background-repeat: no-repeat;
    background-position-x: -7rem;
}
</style>