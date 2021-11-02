<template>
  <v-app id="app">
    <cb-m-frame-system-bar />
    <cb-m-frame-app-bar />
    <v-main>
        <Nuxt />
    </v-main>
    <cb-m-frame-footer />
  </v-app>
</template>

<script>
export default {
  name: "landing"
};
</script>

<style>
#app {
  background-color: #1d1d1e;
}
</style>
