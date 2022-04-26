<template>
   <div class="container_projects">

      <!-- The project description section -->
      <div class="project_info">
         <h3 style="font-weight: bold;">{{ selected_proj.title }}</h3>
         <section class="general_proj_info">
            <img src="../assets/logo.png" />
            <div>
               <h6 style="font-weight: bold;">DESCRIPTION</h6>
               <p style="margin-inline: 1rem;">{{ selected_proj.description }}</p>
            </div>
         </section>
         <section class="proj_redirects">
            <a href="">Git</a>
            <a :href="selected_proj.link">Link</a>
         </section>
      </div>

      <div name="Projects_List" class="wrapper">
         <select id="projs" size="18" class="projects_list" v-model="current_project">
            <option v-for="proj of projects" :key=proj.title :value=projects.indexOf(proj.title) class="select_option">
               {{ proj.title }}
            </option>
         </select>
         <p>{{ selected_proj.title }}</p>
      </div>

   </div>
</template>

<script>
export default {
   data() {
      return {
         selected_proj: {},
         projects: [
            {
               title: "hi",
               description: "lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
               github: "",
               link: "",
               date_start: "",
               date_end: "",
            },
            {
               title: "not hello",
               description: "lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
               github: "",
               link: "",
               date_start: "",
               date_end: "",
            },
            {
               title: "not hello 2",
               description: "",
               github: "",
               link: "",
               date_start: "",
               date_end: "",
            }
         ],
      }
   }
}
</script>

<style>
.container_projects {
   border: 1px solid black;
   margin-bottom: 1%;
   margin-inline: 4rem;
   display: flex;
   justify-content: left;
   align-items: center;
}

.project_info {
   border: 1px solid black;
   justify-content: center;
   text-align: center;
   max-width: 30%;
   padding-top: 0.1%;
}

.general_proj_info {
   display: inline;
   justify-content: left;
   align-items: center;
}

.general_proj_info img {
   border: 1px solid black;
   margin-inline: 1rem;
   height: 20%;
   width: 30%;
   margin-bottom: 1em;
   justify-content: center;
   align-items: center;
}

.projects_list {
   scrollbar-color: var(--nav-background) var(--footer-text-color);
   background-color: transparent;
   border: 1px solid black;
   margin-left: 10px;
   height: max-content;
   padding: 2px;
}

.proj_redirects {
   display: inline;
   justify-content: center;
   text-align: center;
}

.proj_redirects a {
   margin-inline: 1rem;
}

.select_option {
   background: grey;
   color: white;
}
</style>