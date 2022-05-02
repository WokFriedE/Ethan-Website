<template>
  <span>
    <navBarVue />
    <div
      style="height: 2rem;  background: linear-gradient(180deg, rgba(120, 120, 120, 1) 20%, rgba(255, 255, 255,0) 90%); " />
    <profileMainVue />
    <projectsVue />
    <boxListingsVue />
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

export default {
  components: {
    navBarVue,
    profileMainVue,
    projectsVue,
    boxListingsVue,
    footerVue,
  },
};

//add scroll open effect
</script>

<style>
body {
  background-color: rgb(70, 70, 70);
  margin: 0%;
}

.header {
  text-align: center;
  color: rgb(214, 214, 214);
  font-size: 40px;
  text-decoration: underline;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
}
</style>

