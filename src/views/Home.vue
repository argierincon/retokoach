<template>
  <div class="about">
    <Drawer />
    <Container>
      <div class="margin3">
        <UserName />
      </div>
      <GraphContainer />
      <ResultsContainer />
    </Container>
  </div>
</template>

<script>
import Container from "../components/Container";
import Drawer from "../components/Drawer";
import UserName from "../components/UserName";
import GraphContainer from "../components/GraphContainer";
import ResultsContainer from "../components/ResultsContainer";

export default {
  name: "About",
  components: {
    Container,
    Drawer,
    UserName,
    GraphContainer,
    ResultsContainer,
  },
};
</script>

<style>
.about {
  display: flex;
}

.margin3 {
  margin-left: 5%;
  margin-bottom: 2%;
}
</style>
