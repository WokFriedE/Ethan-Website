<template>
    <div>
        <h3 class="section-head">
            {{ info.title }}
        </h3>

        <div class="centering" style="margin-bottom:0.5rem;" v-if="hasDescription">
            <span>Show Description?</span>
            <label class="switch">
                <input type="checkbox" v-model="showDescription">
                <span class="slider round"></span>
            </label>

        </div>

        <ul class="infomation-box">
            <li class="info-item" v-for="item in data" :key="item.name">
                {{ item.name }}
                <h6 v-if="item.description !== '' && showDescription">Description:</h6>
                <p v-if="item.description !== '' && showDescription">{{ item.description }}</p>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    props: ['propsdata'],
    data() {
        return {
            info: this.propsdata[0],
            data: this.propsdata[1],
            hasDescription: this.propsdata[0].hasDescription,
            showDescription: false,
        };
    },
    methods: {
        prints: function (item) {
            console.log(item);
        }
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
    margin-inline: 1rem;
    border: 1px solid rgba(0, 0, 0, 0.1);
    padding: 1%;
}

.info-item {
    margin: 5px;
    margin-top: 0%;
    padding: 5px;
    padding-inline: 10px;
    border-radius: 2px;
    background-color: rgba(95, 95, 95, 0.5);
    color: rgb(228, 228, 228);
    font-weight: bold;
    max-height: 8rem;
}

.info-item h6,
.info-item p {
    margin: 0%;
    font-weight: none;
    height: 100%;
    overflow-y: auto;
    scrollbar-color: var(--nav-background) var(--footer-text-color);

}

.info-item:hover {
    transform: scale(1.2);
    background-color: rgba(70, 70, 70, 1);
}

/* sliders */

.switch {
    position: relative;
    display: inline-block;
    width: 60px;
    height: 34px;
    margin-inline: 1%;
    transform: scale(0.75);
}

.swtich input {
    opacity: 0;
    width: 0;
    height: 0;
}

.slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgb(119, 119, 119);
    -webkit-transition: .2s;
    transition: .2s;
}

.slider::before {
    position: absolute;
    content: "";
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: rgb(197, 197, 197);
    -webkit-transition: .2s;
    transition: .2s;
}


input:checked+.slider {
    background-color: #2471b1;
}



input:checked+.slider:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
}
</style>