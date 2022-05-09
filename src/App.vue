<template>
  <span>
    <navBarVue />
    <div
      style="height: 2rem;  background: linear-gradient(180deg, rgba(120, 120, 120, 1) 20%, rgba(255, 255, 255,0) 90%); " />
    <profileMainVue />
    <projectsVue />
    <div style="display: flex; align-items:center; justify-content: center;">
      <section style="width:50%;">
        <boxListingsVue v-bind:propsdata="languages" />
      </section>
      <section style="width:50%">
        <boxListingsVue v-bind:propsdata="skills" />
      </section>
    </div>
    <boxListingsVue v-bind:propsdata="classes" />

    <div style="height: 2rem;  background: linear-gradient(0deg, dimgrey 20%, rgba(255, 255, 255,0) 60%); " />
    <footerVue />
  </span>
</template>

<script>
import navBarVue from "./components/Nav-Bar.vue";
import profileMainVue from "./components/Profile-Main.vue";
import projectsVue from "./components/Projects-Main.vue";
import boxListingsVue from "./components/Box-Listings.vue";
import footerVue from "./components/Footer-Main.vue";

import skills from "./data/skills.json";
import languages from "./data/languages.json";
import classes from "./data/classes.json";

export default {
  components: {
    navBarVue,
    profileMainVue,
    projectsVue,
    boxListingsVue,
    footerVue,
  },

  data() {
    return {
      skills: skills,
      classes: classes,
      languages: languages
    };
  },
};

//add scroll open effect
</script>

<style>
body {
  background-color: rgb(177, 177, 177);
  margin: 0%;
}
</style>

