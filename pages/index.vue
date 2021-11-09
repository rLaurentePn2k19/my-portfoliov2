<template>
  <div>
    <cb-o-my-home-temp-2 id="home" />
    <cb-o-my-about-me-temp-1 id="about-me" />
    <cb-o-my-skills-temp-1 id="skills" />
    <cb-o-my-projects-temp-1 id="projects" />
    <cb-o-my-experience-temp-1 id="experience" />
    <cb-o-my-have-any-temp-1 id="any-projects" />
    <cb-o-my-contact-me-temp-1 id="contact" />
    <cb-a-floating-button :formActions="formActions" />
  </div>
</template>

<script>
export default {
  layout: "landing",
  data() {
    return {
      formActions: [
        {
          name: "Go Up",
          icon: "mdi-chevron-up",
          color: "my_primary"
        }
      ]
    };
  }
};
</script>
