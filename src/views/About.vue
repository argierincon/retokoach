<template>
  <div class="about">
    <Drawer />
    <Container>
      <router-link to="/">
        <BtnBack />
      </router-link>
      <div class="adviser-report">
        <UserName greeting="Asesor:" :userName="$route.params.name" />
        <SecondaryBtn />
      </div>
      <div>
        <ResultsContainer
          title="Lista de Indicadores"
          :mainbtn="true"
          :search="false"
          :overview="false"
          :adviser="true"
        />
        <ResultsContainer
          title="Cuadro evolutivo"
          :mainbtn="false"
          :search="false"
          :overview="false"
          :adviser="true"
        />
      </div>
      <div class="adv-graph">
        <AdviserGraph />
      </div>
    </Container>
  </div>
</template>

<script>
import Container from "../components/Container";
import BtnBack from "../components/BtnBack";
import SecondaryBtn from "../components/SecondaryBtn";
import Drawer from "../components/Drawer";
import UserName from "../components/UserName";
import ResultsContainer from "../components/ResultsContainer";
import AdviserGraph from "../components/AdviserGraph";

export default {
  name: "About",
  components: {
    Container,
    BtnBack,
    SecondaryBtn,
    Drawer,
    UserName,
    ResultsContainer,
    AdviserGraph,
  },
};
</script>

<style>
.about {
  display: flex;
  justify-content: center;
}

.adviser-report {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 80%;
  margin-left: 3%;
}

.adv-graph {
  margin: 4% 0;
}

a {
  text-decoration: none !important;
}
</style>
