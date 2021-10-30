<template>
  <v-container fluid fill-height class="my-16">
    <v-row align="center">
      <v-col cols="12">
        <v-card flat color="transparent" class="mx-auto" max-width="600">
          <div class="d-flex justify-center">
            <picture>
              <v-img
                width="200"
                src="/img/flipped-rangie.png"
                lazy-src="/img/programmer.png"
                alt="programmer"
              />
            </picture>
          </div>
          <v-card-title class="d-flex justify-center">
            <div class="display-3 white--text">Hi, I'm Rangie!</div>
          </v-card-title>
          <v-card-subtitle class="d-flex justify-center">
            <div class="display-2 white--text">I am a Web Developer.</div>
          </v-card-subtitle>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="my_secondary" class="rounded-lg pa-5 text-capitalize button white--text font-weight-black">Github</v-btn>
            <v-btn color="my_secondary" class="rounded-lg pa-5 text-capitalize button white--text font-weight-black">Resume</v-btn>
            <v-spacer></v-spacer> 
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'home'
};
</script>
