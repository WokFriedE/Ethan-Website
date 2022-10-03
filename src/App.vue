<template>
  <span>

    <nav>
      <p> hi </p>
    </nav>

    <router-view />
  </span>
</template>

<script>
import skills from "./data/skills.json";
import languages from "./data/languages.json";
import classes from "./data/classes.json";

export default {
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

