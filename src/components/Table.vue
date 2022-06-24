<template>
    <div class="table">
        <div class="row">
            <div class="column">
                <div class="title">Channel</div>
            </div>
            <div class="column">
                <div class="title">Details</div>
            </div>
            <div class="column">
                <div class="title">Number of items</div>
            </div>
            <div class="column">
                <div class="title">Low complexity</div>
            </div>
            <div class="column">
                <div class="title">Medium complexity</div>
            </div>
            <div class="column">
                <div class="title">High complexity</div>
            </div>
        </div>
        <TableLine channel="Broadcast Email"
                    details="Creation and sending of a new broadcast email"
                    :nbOfItems="1"
                    :lowPrice="300"
                    :midPrice="350"
                    :hiPrice="400" />
        <TableLine channel="Online Ads"
                    details="Creation and display of an online banner (CPM)"
                    :nbOfItems="2"
                    :lowPrice="200"
                    :midPrice="300"
                    :hiPrice="350" />
        <TableLine channel="Website"
                    details="Creation a new website (cost per webpage)"
                    :nbOfItems="1"
                    :lowPrice="500"
                    :midPrice="700"
                    :hiPrice="900" />
        <div class="totals">
            <div class="total-column low">
                Total estimated cost
            </div>
            <div class="total-column price">
                1200 €
            </div>
            <div class="total-column price">
                1650 €
            </div>
            <div class="total-column price">
                2000 €
            </div>
        </div>
    </div>
</template>

<script>
import TableLine from './TableLine.vue'
export default {
  name: 'Table',
  components: {
    TableLine,
  }
}
</script>

<style scoped>
.table {
    position: relative;
    border-radius: 10px 10px 0px 10px;
    background-color: #fff;
    box-shadow: 2px 2px 2px 2px #e8e9e8;
}
.totals {
    position: absolute;
    right: 0;
    border-radius: 0 0 10px 10px;
    background-color: #daf1e3;
    display: grid;
    grid-auto-flow: column;
    grid-template-columns: calc(23.3% - 1px) 24.3% 23.6% 1fr;
    box-shadow: 2px 2px 2px 2px #e8e9e8;
    font-weight: bold;
    width: 57.8%;
}
.row {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr 1fr 1fr 1fr;
    grid-auto-flow: column;
    padding: 16px;
    border-bottom: 1px solid #e8e9e8;
}
.title {
    font-weight: bold;
    border-bottom: 1px #f9faf9;
}
.total-column {
    padding: 16px;
}
.price {
    margin-left: 18%;
}
</style>
