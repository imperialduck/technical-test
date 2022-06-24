<template>
    <div class="row">
        <div class="channel">
            {{channel}}
        </div>
        <div>
            {{details}}
        </div>
        <Counter v-if="nbOfItems" :nb-of-items="nbOfItems" />
        <div class="price">
            {{lowPrice}}
        </div>
        <div class="price">
            {{midPrice}}
        </div>
        <div class="price">
            {{hiPrice}}
        </div>
    </div>
</template>

<script>
import Counter from './Counter.vue'
export default {
    name: "TableLine",
    props: {
        channel: String,
        details: String,
        nbOfItems: Number,
        lowPrice: Number,
        midPrice: Number,
        hiPrice: Number,
    },
    components: {
        Counter,
    }
}
</script>

<style scoped>
    div {
        font-size: 14px;
        color: #555555;
    }
    .price {
        margin-left: 18%
    }
    .row {
        display: grid;
        grid-auto-flow: column;
        grid-template-columns: 1fr 2fr 1fr 1fr 1fr 1fr;
    }
    .channel {
        font-weight: bold;
    }
</style>
