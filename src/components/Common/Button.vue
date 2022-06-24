<template>
  <button class="button">
    {{label}}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    label: String,
  }
}
</script>

<style>
    button {
        position: relative;
        padding: 12px 48px 12px 48px;
        background-color: #00916e;
        border: none;
        border-radius: 10px;
        color: #fff;
    }
    button:hover {
        cursor: pointer;
    }
</style>
