<template>
    <div class="container_profile">
        <img src="https://media-exp1.licdn.com/dms/image/C4E03AQHJ_7jj6R_BZg/profile-displayphoto-shrink_200_200/0/1650336371998?e=1655942400&v=beta&t=9GBhhTk71qXuNxNJjUrs5SdJ-erDdwa_9Th5jQRCWiI"
            class="profile_pic" />
        <div class="profile_info">
            <h2 class="profile_name">Ethan Ho</h2>
            <h3 class="profile_title">Computer Science, B.S.</h3>
            <h4 class="profile_location">New Jersey, USA</h4>
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
    border-radius: 25%;
    border: 2px solid rgba(214, 214, 214, 0.5);
}

.profile_info {
    margin: 2%;
}
</style>