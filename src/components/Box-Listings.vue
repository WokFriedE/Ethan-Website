<template>
    <div>
        <h3 class="section-head">
            {{ info.title }}
        </h3>
        <ul class="infomation-box">
            <li class="info-item" v-for="item in data" :key="item.name"> {{ item.name }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    props: ['propsdata'],
    data() {
        return {
            info: this.propsdata[0],
            data: this.propsdata[1]
        };
    },
};
</script>

<style>
.infomation-box {
    display: flex;
    list-style: none;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    margin-inline: 5rem;
}

.info-item {
    margin: 5px;
    margin-top: 0%;
    padding: 5px;
    padding-inline: 10px;
    border-radius: 2px;
    background-color: rgba(70, 70, 70, 0.5);
    color: rgb(236, 236, 236);
}

.info-item:hover {
    transform: scale(1.2);
    background-color: rgba(70, 70, 70, 1);

}
</style>