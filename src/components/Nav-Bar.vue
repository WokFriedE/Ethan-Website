<template>
    <nav>
        <button class="resume-button">
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

.resume-button {
    background-color: rgb(197, 196, 196);
    border-radius: 10px;
    margin: 1rem;
    margin-bottom: 0.05%;
    padding: 0.5%;
    padding-inline: 1%;
    color: rgb(92, 92, 92);
}

.resume-button:hover {
    background-color: rgb(83, 83, 83);
    color: #ffffff;
    animation: raiseUp 100ms ease-in;
    transform: scale(1.1);
}

.resume-button:not(:hover) {
    animation: goDown 100ms ease-in;
    transform: scale(1);
}
</style>