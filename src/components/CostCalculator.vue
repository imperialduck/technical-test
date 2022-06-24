<template>
    <div>
        <h1 class="title">{{title}}</h1>
        <p class="breadcrumbs">{{breadcrumbs}}</p>
        <Table />
        <div class="bottom-buttons">
            <Button label="Back" class="back" />
            <Button label="Submit" class="submit" />
        </div>
    </div>
</template>

<script>
import Table from './Table'
import Button from './Common/Button.vue'
export default {
  name: 'CostCalculator',
  components: {
    Table,
    Button
},
  data () {
    return {
      title: 'Page Title / Cost Calculator',
      breadcrumbs: 'Dashboard > tools > cost',
    }
  }
}
</script>

<style scoped>
.title {
  font-weight: bolder;
  font-size: 24px;
}
.breadcrumbs {
    margin-top: 8px;
    margin-bottom: 64px;
    /* semi-bold does seem to exist, so i went for bolder and bold instead */
    font-weight: bold;
    color: #555555;
}
.bottom-buttons {
    margin-top: 200px;
    display: grid;
    grid-template-columns: 1fr 1fr;
}
.back {
    justify-self: left;
}
.submit {
    justify-self: right;
}
</style>
