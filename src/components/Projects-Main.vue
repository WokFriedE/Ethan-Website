<template>
    <span>
        <strong>HI</strong>
        <div class="project-title" v-for="proj in projects" v-bind:key="proj.name">
            <ul>
                <li> {{ proj.name }} </li>
                <li>{{ proj.description }}</li>
            </ul>
        </div>
    </span>
</template>

<script>
export default {

    data() {
        return {
            projects: [
                {
                    name: 'Personal Website',
                    description: 'A website that I built for myself to showcase my projects and learn new things.',
                    link: '',
                    img: ''
                },
                {
                    name: 'Personal Website',
                    description: 'A website that I built for myself to showcase my projects and learn new things.',
                    link: '',
                    img: ''
                },
            ]
        }
    }
}
</script>

<style>
</style>