<template>
    <div class="card">
        <div class="card-front">

        </div>
    </div>
</template>

<script>
export default {
    props: ['name', 'description', 'img', 'start', 'end', 'link'],
};
</script>

<style>
.card {
    background-color: var(--nav-background);
    border-radius: 4px;
    box-shadow: 0px 0px 3px rgba(0, 0, 0, 0.2);
    height: 250px;
    width: 250px;
}
</style>