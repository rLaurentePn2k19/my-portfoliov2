<template>
  <div class="about-me">
    <v-container class="my-16">
      <v-row class="py-16">
        <v-col cols="12" md="6" class="d-flex justify-start align-center ">
          <div class="display-3 white--text">
            <div class="mb-4">About Me</div>
            <v-divider v-for="i in 5" :key="i" class="my_primary"></v-divider>
          </div>
        </v-col>
        <v-col cols="12" md="6">
          <blockquote class="headline white--text text-justify">
            I graduated as scholar of
            <a
              target="_blank"
              href="https://www.passerellesnumeriques.org/en/"
              class="my_primary--text text-decoration-none font-weight-bold"
            >
              Passerelles numeriques Philippines
            </a>
            a French NGO, at the University of San Carlos - Talamban Campus with
            the course of Certificate of Computer Technology (CCT) major in
            Software Development. Programming is really one of passion aside
            from that, I also love playing Sports and Online Games.
          </blockquote>
          <div class="mt-12">
            <v-hover v-slot="{ hover }">
              <v-btn
                width="30%"
                :outlined="hover"
                height="70"
                color="my_primary"
                class="
                  rounded-lg
                  title
                  white--text
                  font-weight-black
                  text-capitalize
                "
                @click="goToWorkExperiences"
              >
                View Works
              </v-btn>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-btn
                width="30%"
                height="70"
                class="
                  rounded-lg
                  mx-2
                  white--text
                  text-capitalize
                  title
                  font-weight-black
                "
                :outlined="!hover"
                color="my_primary"
                href="/img/dev-rangie-resume.pdf"
                target="_blank"
              >
                Download CV
              </v-btn>
            </v-hover>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "aboutMe",
  methods: {
    goToWorkExperiences() {
      this.$vuetify.goTo("#experience", {
        duration: 700,
        offset: 0,
        easing: "easeInOutCubic"
      });
    }
  }
};
</script>

<style scoped>
.about-me {
  background-color: #2b2c2c;
}

blockquote {
  border-left: 5px solid #2f6e77;
  padding-left: 20px;
}

.v-divider {
  width: 60%;
}
</style>