<template>
  <section class="container-graph">
    <div class="items-graph">
      <TitleSection name="Panel de indicadores" />
      <IndicatorsFilter />
    </div>
    <div class="indicator-chart">
      <GraphCard name="Cantidad de ventas por hora" />
      <GraphCard name="AHT" />
      <GraphCard name="Ventas Acumuladas" />
      <GraphCard name="Ventas Concretadas" />
    </div>
  </section>
</template>

<script>
import TitleSection from "../components/TitleSection";
import GraphCard from "../components/GraphCard";
import IndicatorsFilter from "../components/IndicatorsFilter";

export default {
  components: {
    TitleSection,
    GraphCard,
    IndicatorsFilter,
  },
};
</script>

<style>
.container-graph {
  margin: auto;
  width: 90%;
}

.items-graph {
  display: flex;
  justify-content: space-between;
}

.indicator-chart {
  display: flex;
  justify-content: space-evenly;
}
</style>