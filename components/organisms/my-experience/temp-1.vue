<template>
  <v-container fill-height class="my-16">
    <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <div class="white--text display-3 text-center">
          <div class="mb-4">Work Experiences</div>
          <v-divider
            v-for="i in 5"
            :key="i"
            class="mx-16 my_primary"
          ></v-divider>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex justify-center">
        <blockquote class="white--text headline text-center">
          Excepteur sint occaecat cupidatat non proident, sunt in culpa qui
          officia deserunt mollit anim id est laborum. Sed ut perspiciatis unde
          omnis iste natur
        </blockquote>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <div class="mt-10">
          <v-slide-group
            v-model="model"
            active-class="success"
            :show-arrows="false"
            center-active
          >
            <v-slide-item
              v-for="(work, i) in works"
              :key="i"
              v-slot="{ active, toggle }"
            >
              <v-card
                :color="active ? 'my_primary' : 'transparent'"
                class="pa-4 rounded-0"
                height="500"
                width="380"
                @mouseenter="toggle"
                :flat="!active"
                :elevation="active ? '24' : '0'"
              >
                <v-card-title class="d-flex justify-start white--text mt-6">
                  <div class="subtitle-1 font-weight-light">
                    {{ work.date }}
                  </div>
                </v-card-title>
                <v-card-subtitle class="white--text">
                  <div class="headline font-weight-bold mt-2">
                    {{ work.title }}
                  </div>
                  <div class="subtitle-1 font-weight-light mt-2">
                    {{ work.company }}
                  </div>
                </v-card-subtitle>

                <v-card-text class="white--text px-4">
                  <v-row>
                    <v-col cols="12" class="d-flex justify-center">
                      <div class="title font-weight-light text-justify">
                        <blockquote>
                          {{ work.description }}
                        </blockquote>
                      </div>
                    </v-col>
                  </v-row>
                </v-card-text>
              </v-card>
            </v-slide-item>
          </v-slide-group>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "jobExperience",
  data: () => ({
    model: null,
    works: [
      {
        date: "March 2021 - Present",
        company: "CrewBloom Inc.",
        title: "Web Developer",
        description: "Currently working as Full-Stack Web Developer, using NuxtJs-Strapi-MySQL."
      },
      {
        date: "December 2020 - April 2021",
        company: "Softype Philippines Inc.",
        title: "Technical Consultant",
        description: "I was an Oracle NetSuite Technical Consultant/Developer, I make NetSuite Customization Processess using SuiteScript 1.x, 2.x, and solved any issue related to technical that client encountered."
      },
      {
        date: "June 2020 - August 2020",
        company: "Increment Technologies",
        title: "Web Developer",
        description:
          "I was once a volunteer Web Developer, which I helped to develop an Application for Contact Tracing of COVID-19."
      }
    ]
  })
};
</script>

<style scoped>
.btn {
  position: absolute;
  bottom: 2rem;
}

.v-card.v-sheet.theme--light {
  border: 1px solid #3d3d3d !important;
}
</style>