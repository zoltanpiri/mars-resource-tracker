<template>
    <div class="container">
        <div v-if="extended" class="btn btn10" @click="decrement10">-10</div>
        <div class="btn" @click="decrement">-</div>
        <div class="counter">{{ n }}</div>
        <div class="btn" @click="increment">+</div>
        <div v-if="extended" class="btn btn10" @click="increment10">+10</div>
    </div>
</template>

<script>
    export default {
        name: "TrackCounter",
        props: {
            extended: {
                type: Boolean,
                default: false
            }
        },
        data() {
            return {
                n: 0
            }
        },
        methods: {
            increment() {
                this.n++;
            },
            decrement() {
                this.n--;
            },
            increment10() {
                this.n += 10;
            },
            decrement10() {
                this.n -= 10;
            }
        }
    }
</script>

<style scoped>
    .container{
        width: 170px;
        display: flex;
        justify-content: space-around;
        font-size: 1.6em;
    }
    .btn {
        border: 2px solid darkgray;
        border-radius: 10px;
        width: 30px;
        height: 30px;
        cursor: pointer;
    }
    .btn10 {
        font-size: 12px;
        padding-top: 8px;
        height: 22px;
    }
    .counter {
        width:50px
    }
</style>