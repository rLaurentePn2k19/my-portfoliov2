<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="12" class="d-flex justify-center">
          <picture>
            <v-img
              width="150"
              src="/img/my-logo-1-removebg-preview.png"
              lazy-src="/img/my-logo-1-removebg-preview.png"
            >
            </v-img>
          </picture>
        </v-col>
        <v-col cols="12">
          <div class="title white--text text-center px-16 mx-16">
            <em>
              <q> Code is like humor. When you have to explain it, it’s bad.</q>
              – Cory House
            </em>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <v-footer padless color="background" class="py-4" height="100">
      <v-col cols="12">
        <v-divider class="my_primary"></v-divider>
      </v-col>
      <v-col class="text-center" cols="12">
        <div class="white--text subtitle-1">
          Copyright © 2021 NuxtJs + Vuetify | Dev Rangie
        </div>
      </v-col>
    </v-footer>
  </div>
</template>

<script>
export default {
  name: "footer"
};
</script>
