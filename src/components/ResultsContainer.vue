<template>
  <section class="container-graph margin">
    <div class="btn-search">
      <TitleSection :name="title" />
      <div>
        <MainBtn v-if="mainbtn" />
        <Search v-if="search" />
      </div>
    </div>
    <TeamResultsTable v-if="overview" />
    <AdviserTable v-if="adviser" />
  </section>
</template>

<script>
import TitleSection from "./TitleSection";
import MainBtn from "../components/MainBtn";
import Search from "../components/Search";
import TeamResultsTable from "../components/TeamResultsTable";
import AdviserTable from "../components/AdviserTable";

export default {
  props: {
    title: {
      type: String,
      default: "Resultados del Equipo",
    },
    mainbtn: {
      type: Boolean,
      default: true,
    },
    search: {
      type: Boolean,
      default: true,
    },
    overview: {
      type: Boolean,
      default: true,
    },
    adviser: {
      type: Boolean,
      default: false,
    },
  },
  components: {
    TitleSection,
    MainBtn,
    Search,
    TeamResultsTable,
    AdviserTable,
  },
};
</script>

<style>
.container-graph {
  width: 90%;
}

.btn-search {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 4% 0;
}

.btn-search > p {
  margin: 0;
}

.btn-search > div {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
</style>