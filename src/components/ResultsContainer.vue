<template>
  <section class="container-graph margin">
    <TitleSection name="Resultados del Equipo" />
    <div class="btn-search">
      <MainBtn />
      <Search />
    </div>
  </section>
</template>

<script>
import TitleSection from "./TitleSection";
import MainBtn from "../components/MainBtn";
import Search from "../components/Search";

export default {
  components: {
    TitleSection,
    MainBtn,
    Search,
  },
};
</script>

<style>
.margin {
  margin: 3% 0;
}

.btn-search {
  display: flex;
  justify-content: flex-end;
}
</style>