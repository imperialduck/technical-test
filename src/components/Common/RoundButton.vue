<template>
    <button class="button" :onClick="handleClick">
        <div class="button-label">{{label}}</div>
    </button>
</template>

<script>
export default {
    name: 'Counter',
    props: {
        label: String,
        className: String,
        handleClick: Function,
    },
}

</script>

<style scoped>
div {
    font-weight: bold;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    margin-top: 3px;
}
</style>
