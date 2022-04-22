<template>
  <span>
    <div style="height: 1rem; background-color: rgba(0,85,102,0.5)" />
    <profileMainVue />
    <projects />
    <foot />
  </span>
</template>

<script>
import profileMainVue from "./components/Profile-Main.vue";
import projects from "./components/Projects-Main.vue";
import foot from "./components/Footer-Main.vue";

export default {
  components: {
    profileMainVue,
    projects,
    foot,
  },
};

//fix footer, add scroll open effect
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

