<template>
    <div class="container_projects">

        <!-- The project description section -->
        <div class="project_desc">
            <h3 style="font-weight: bold;">Project Title</h3>
            <section class="general_proj_info">
                <img src="../assets/logo.png"
                    style="border: 1px solid black; margin-inline: 1rem; height: 20%; width: 30%; object-fit: contain;" />
                <div>
                    <h6 style="font-weight: bold;">Description:</h6>
                    <p style="margin-inline: 1rem;">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tenetur
                        quae
                        placeat cumque fuga voluptatem
                        temporibus, doloribus laboriosam nostrum et natus ex vero quos vel! Recusandae aliquam rem iure
                        sequi
                        odit.</p>
                </div>
            </section>
            <section class="center">
                <a href="">Git</a>
                <a href="">Link</a>
            </section>
        </div>



    </div>
</template>

<script>
export default {
    data() {
        return {
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

.project_desc {
    border: 1px solid black;
    justify-content: center;
    text-align: center;
    max-width: 30%;
    padding-top: 0.1%;
}

.center a {
    margin-inline: 1rem;
}

.general_proj_info {
    display: inline;
    justify-content: left;
    align-items: center;
    margin-inline: 1rem;
}
</style>