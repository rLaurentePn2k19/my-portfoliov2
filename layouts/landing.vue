<template>
  <v-app id="app">
    <cb-m-frame-system-bar />
    <cb-m-frame-app-bar />
    <v-main>
        <Nuxt />
    </v-main>
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
  height: 200vh;
}
</style>
