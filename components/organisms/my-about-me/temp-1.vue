<template>
  <v-container fluid class="about-me pa-16 my-16">
    <v-row>
      <v-col cols="12" md="6" class="d-flex justify-center align-center">
        <div class="display-3 white--text">
          <div class="mb-4">About Me</div>
          <v-divider
            v-for="i in 5"
            :key="i"
            class="my_primary"
          ></v-divider>
        </div>
      </v-col>
      <v-col cols="12" md="6">
        <blockquote class="headline white--text">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nu
          pariatur excepteur sint occaecat.
        </blockquote>
        <div class="mt-12">
            <v-hover v-slot="{ hover }">
                <v-btn width="30%" :outlined="hover" height="70" color="my_primary" class="rounded-lg title white--text font-weight-black text-capitalize">
                    View Works
                </v-btn>
            </v-hover>
            <v-hover v-slot="{ hover }">
                <v-btn width="30%" height="70" class="rounded-lg mx-2 white--text text-capitalize title font-weight-black" :outlined="!hover" color="my_primary">
                    Download CV
                </v-btn>
            </v-hover>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
.about-me {
  background-color: #2b2c2c;
  height: 50vh;
}

blockquote {
  border-left: 5px solid #2f6e77;
  padding-left: 20px;
}

.v-divider{
    width: 60%;
}
</style>