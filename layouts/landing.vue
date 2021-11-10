<template>
  <v-app id="app">
    <transition name="fade">
      <div v-if="!isLoading">
        <cb-m-frame-system-bar />
        <cb-m-frame-app-bar />
        <v-main>
          <Nuxt />
        </v-main>
        <cb-m-frame-footer />
      </div>
    </transition>
    <div v-if="isLoading">
      <cb-a-loading />
    </div>
  </v-app>
</template>

<script>
export default {
  name: "landing",
  data() {
    return {
      isLoading: true
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.isLoading = true;
      this.$nuxt.$loading.start();

      setTimeout(() => {
        this.$nuxt.$loading.finish();
        this.isLoading = false;
      }, 3500);
    });
  }
};
</script>

<style>
#app {
  background-color: #1d1d1e;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

</style>
