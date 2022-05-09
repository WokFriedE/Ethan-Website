<template>
    <div class="container_profile">
        <!-- Image -->
        <img src="https://media-exp1.licdn.com/dms/image/C4E03AQHJ_7jj6R_BZg/profile-displayphoto-shrink_200_200/0/1650336371998?e=1655942400&v=beta&t=9GBhhTk71qXuNxNJjUrs5SdJ-erDdwa_9Th5jQRCWiI"
            class="profile_pic" />
        <!-- Info about me -->
        <div class="profile_info">
            <h2 class="profile_name">Ethan Ho</h2>
            <h3 class="profile_title">Computer Science, B.S.</h3>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Id magni dicta iste illo debitis similique
                impedit doloribus itaque non aliquam repudiandae vero esse in aliquid saepe, sunt voluptatibus,
                quibusdam dolorum?</p>
        </div>
    </div>
</template>

<script>
export default {
};
</script>

<style>
.container_profile {
    display: flex;
    justify-content: left;
    align-items: center;
    transform: scale(0.9);
}

.profile_pic {
    height: auto;
    width: auto;
    max-width: 250px;
    max-height: 250px;
    border-radius: 25%;
    border: 2px solid rgba(214, 214, 214, 0.5);
}

.profile_info {
    margin: 2%;
    margin-right: 10%;
    color: whitesmoke;
}
</style>