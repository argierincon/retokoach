<template>
  <div class="indicator-chart">
    <GraphCard name="Cantidad de ventas por hora" />
    <GraphCard name="AHT" />
    <GraphCard name="Ventas Acumuladas" />
    <GraphCard name="Ventas Concretadas" />
  </div>
</template>

<script>
import GraphCard from "../components/GraphCard";

export default {
  components: {
    GraphCard,
  },
};
</script>

<style>
.indicator-chart {
  display: flex;
  justify-content: space-evenly;
}
</style>