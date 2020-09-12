<template>
  <div class="adviser-graph">
    <div>
      <TitleSection name="Gráfica" />
    </div>
    <img src="../assets/img/grafica-asesor.png" alt="grafica" />
  </div>
</template>

<script>
import TitleSection from "../components/TitleSection";

export default {
  components: {
    TitleSection,
  },
};
</script>

<style>
.adviser-graph {
  width: 90%;
  margin: auto;
}

.adviser-graph > div {
  margin-bottom: 4%;
}

.adviser-graph > img {
  width: 60%;
}
</style>