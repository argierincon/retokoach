<template>
  <div class="graph">
    <p>{{name}}</p>
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    name: String,
  },
};
</script>

<style>
.graph {
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  width: 20%;
  height: 220px;
  background: #ffffff;
  box-shadow: -2px 0px 4px rgba(0, 0, 0, 0.25), 0px 3px 4px rgba(0, 0, 0, 0.25);
  border-radius: 25px;
  font-size: 16px;
  text-align: center;
  font-weight: bold;
}

.graph > p {
  width: 85%;
}
</style>