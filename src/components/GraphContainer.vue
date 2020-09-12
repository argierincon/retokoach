<template>
  <section class="container-graph">
    <div class="items-graph">
      <TitleSection name="Panel de indicadores" />
      <IndicatorsFilter />
    </div>
    <div class="indicator-chart">
      <GraphCard name="Cantidad de ventas por hora">
        <img src="../assets/img/graph-1.png" />
      </GraphCard>

      <GraphCard name="AHT">
        <img src="../assets/img/graph-2.png" />
      </GraphCard>

      <GraphCard name="Ventas Acumuladas">
        <img src="../assets/img/graph-3.png" />
      </GraphCard>
      
      <GraphCard name="Ventas Concretadas">
        <img src="../assets/img/graph-4.png" />
      </GraphCard>
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
  align-items: center;
  justify-content: space-between;
  margin-bottom: 4%;
}

.indicator-chart {
  display: flex;
  justify-content: space-evenly;
}
</style>