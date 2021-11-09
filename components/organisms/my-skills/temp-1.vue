<template>
  <v-container fill-height class="my-16">
    <v-row>
      <v-col cols="12" class="d-flex justify-center">
        <div class="white--text display-3">
          <div class="mb-4">What I do</div>
          <v-divider
            v-for="i in 5"
            :key="i"
            class="mx-12 my_primary"
          ></v-divider>
        </div>
      </v-col>
      <v-col cols="12" class="d-flex justify-center">
        <blockquote class="white--text headline text-center">
          {{ skillDescription }}
        </blockquote>
      </v-col>
    </v-row>
    <v-row class="mt-10">
      <v-col cols="12" md="6" v-for="(skill, i) in skills" :key="i">
        <v-lazy
          v-model="isActive"
          :options="{
            threshold: 1.0,
          }"
          min-height="200"
          :transition="`scroll-y-transition`"
        >
          <v-card
            height="300"
            :color="skill.color"
            flat
            class="rounded-lg px-16 pt-12"
          >
            <div class="mx-4">
              <picture>
                <v-img width="80" :src="skill.icon" :lazy-src="skill.icon">
                </v-img>
              </picture>
            </div>
            <v-card-title class="display-1 white--text font-weight-bold">
              <div>{{ skill.title }}</div>
            </v-card-title>
            <v-card-text class="white--text subtitle-1 font-weight-bold">
              <blockquote>
                {{ skill.description }}
              </blockquote>
            </v-card-text>
          </v-card>
        </v-lazy>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "skills",
  data() {
    return {
      isActive: false,
      skillDescription: 'For 1 year of experience in the IT Industry, I developed this set of skills, and looking forward to learn new and improved my technical skills.',
      skills: [
        {
          title: "UI Interface",
          color: "#f9be35",
          icon: "/img/menu-white.png",
          description: `I make Web UI Interface from the submitted design of the Web Designer.`
        },
        {
          title: "Web Development",
          color: "#3db7fc",
          icon: "/img/web-dev.png",
          description: `Mainly Using JS Frameworks for Front-End, PHP Laravel and NodeJs for Back-End. MySQL for DBMS.`
        }
      ]
    };
  }
};
</script>

