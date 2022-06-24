<template>
    <div class="counter">
        <RoundButton :handle-click="decrement" label="-" />
            <input v-model="nbOfItems">
        <RoundButton :handle-click="increment" label="+" />
    </div>
</template>

<script>
import RoundButton from './Common/RoundButton.vue'
export default {
    name: "Counter",
    components: {
        RoundButton
    },
    props: {
        nbOfItems: Number,
    },
    methods: {
        increment: function () {
            console.log("click increment");
        },
        decrement: function () {
            console.log("click decrement")
        }
    },
}
</script>

<style scoped>
.counter {
    border-radius: 10px;
    border: 2px solid lightgray;
    width: fit-content;
    padding: 8px;
    margin-top: -8px;
    margin-bottom: -8px;
    display: inline-flex;
    align-items: center;
}
.minus-button {
    margin-left: 4px;
    margin-right: 10px;
}
.plus-button {    
    margin-left: 10px;
    margin-right: 4px;
}
input {
    margin-right: 8px;
    margin-left: 8px;
    width: 8px;
    align-self: center;
    border: none;
}
.button {
    position: relative;
    display: inline-block;
    padding: 6px;
    border-radius: 10px;
    background-color: #00916e;
    color: #fff;
    border: none;
    height: 21px;
    width: 21px;
    justify-self: center;
    align-self: center;
}
.button-label {
    font-weight: bold;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    margin-top: 3px;
}
</style>
