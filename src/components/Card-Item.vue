<template>
    <div class="card-item" v-on:click="flipCard">
        <div class="card-inner">
            <div class="card-front">
                <p>hi</p>
            </div>
            <div class="card-back">
                <p>back</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['name', 'description', 'img', 'start', 'end', 'link'],
    data() {
        return {
            frontState: true
        }
    },
    methods: {
        flipCard: function () {
            this.frontState = !this.frontState;
            console.log(this.frontState)
        }
    }
};
</script>

<style>
.card-item {
    background-color: transparent;
    border-radius: 4px;
    box-shadow: 0px 0px 3px rgba(0, 0, 0, 0.2);
    height: 200px;
    width: 200px;
    perspective: 1000px;
}

.card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.5s;
    transform-style: preserve-3d;
}

.card-item:hover,
.card-inner {
    transform: rotateY(180deg);
}

.card-front,
.card-back {
    position: absolute;
    width: 100%;
    height: 100%;
}

.card-front {
    background-color: red;

}

.card-back {
    background-color: blue;
    color: white;
}
</style>