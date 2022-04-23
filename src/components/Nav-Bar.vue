<template>
    <nav>
        <button class="resume">
            Resume
        </button>
    </nav>
</template>

<script>
export default {

};
</script>

<style>
nav {
    background-color: var(--nav-background);
    display: flex;
    justify-content: right;
    align-items: right;
}

.resume {
    background-color: rgba(255, 255, 255, 0);
    border-radius: 10px;
    margin: 1rem;
    margin-bottom: 0.05%;
    padding: 0.5%;
    padding-inline: 1%;
    color: rgb(255, 255, 255);
}

.resume:hover {
    background-color: rgba(90, 90, 90, 0.205);
    animation: raiseUp 100ms ease-in;
    transform: scale(1.1);
}

.resume:not(:hover) {
    animation: goDown 100ms ease-in;
    transform: scale(1);
}
</style>