<template>
  <div class="graph">
    <p>{{name}}</p>
    <img src="../assets/img/Group 1135.png" alt="grafico1" />
  </div>
</template>

<script>
export default {
  props: {
    name: String,
  }
};
</script>

<style>
.graph {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  width: 20%;
  height: 220px;
  background: #ffffff;
  box-shadow: 0px 3px 5px rgba(0, 0, 0, 0.25);
  border-radius: 25px;
  font-size: 16px;
  text-align: center;
  font-weight: bold;
}
</style>