<template>
   <div>
      <!-- Header for segment -->
      <h3 class="centering" style="font-weight: bold;">Projects</h3>
      <div style="border-bottom: 2px solid rgba(0, 0, 0, 0.2); max-width: 75%; margin-inline: 10%;" />
      <br />

      <!-- The projects segment -->
      <div class="projects-container">
         <!-- The project description section -->
         <div class="project_info-container">
            <!-- make title scalable -->
            <h4 style="font-weight: bold; margin-top:5px">{{ selected_proj.title }}</h4>
            <!-- Puts the redirect links -->
            <section class="proj_redirects">
               <a v-bind:href="selected_proj.github" v-if="selected_proj.github !== ''" class="proj_redirects-link"
                  target="_blank">GitHub</a>
               <a v-bind:href="selected_proj.link" v-if="selected_proj.link !== ''" class="proj_redirects-link"
                  target="_blank">Project</a>
            </section>
            <!-- general description -->
            <section class="general_proj_info">
               <div>
                  <h6 style="font-weight: bold;" v-if="selected_proj.description !== ''">DESCRIPTION</h6>
                  <p v-if="selected_proj.description !== ''">{{ selected_proj.description }}</p>
               </div>
            </section>
         </div>

         <!-- make custom list -->
         <div class="project_list-container">
            <ul class="projects-list">
               <section class="project-item">
                  <button v-for="proj in projects" :key="projects.indexOf(proj)" v-on:click="handleClick(proj)">
                     {{ proj.title }}
                  </button>
               </section>
            </ul>
         </div>

      </div>
   </div>
</template>

<script>
import json from '../data/projects.json';
console.log(json)

export default {
   data() {
      return {
         projects: json.projects,
         selected_proj: json.projects[0]
      }
   },
   methods: {
      handleClick: function (proj) {
         this.selected_proj = proj;
      }
   },
}
</script>

<style>
/* overall projects containers section */
.projects-container {
   margin-bottom: 1%;
   margin-inline: 4rem;
   display: flex;
   justify-content: left;
   align-items: center;
}

/* project description section */

.project_info-container {
   border: 1px solid rgba(0, 0, 0, 0.3);
   display: inline;
   justify-content: center;
   text-align: center;
   width: 50%;
   margin-top: -15px;
}

.general_proj_info {
   display: flex;
   flex-direction: column;
   justify-content: left;
   align-items: center;
}

.general_proj_info p {
   margin-inline: 1rem;
   height: 10rem;
   scrollbar-color: var(--nav-background) var(--footer-text-color);
   overflow-y: auto;
   padding: 1%;
   border: 1px solid black;
}

.general_proj_info img {
   margin-inline: 1rem;
   height: 6rem;
   width: 15rem;
   margin-bottom: 1rem;
   justify-content: center;
   align-items: center;
}

.proj_redirects {
   margin: 0.5rem;
}

.proj_redirects-link {
   margin: 1rem;
   text-decoration: none;
   color: var(--footer-text-color);
}

/* project list section */

.project_list-container {
   padding-top: 0.1%;
   height: 100%;
   width: 100%;
}

.projects-list {
   border: 1px solid black;
   scrollbar-color: var(--nav-background) var(--footer-text-color);
   overflow-y: scroll;
   overflow-x: hidden;
   height: 280px;
   width: 100%;
   padding-left: 0%;
}

.project-item {
   background-color: var(--nav-background);
}

.project-item button {
   background: none;
   border: none;
   width: 100%;
   text-align: left;
   border-bottom: 1px solid black;
   font-size: medium;
}

.project-item button:hover {
   background-color: grey;
   color: #ffffff;
}
</style>