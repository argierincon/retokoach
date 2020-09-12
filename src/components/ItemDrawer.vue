<template>
  <div class="item-drawer">
    <v-icon medium :color="color">{{icon}}</v-icon>
    <p>{{item}}</p>
  </div>
</template>

<script>
export default {
  props: {
    icon: String,
    item: String,
    color: String,
  },
};
</script>

<style>
.item-drawer {
  display: flex;
  align-items: center;
  width: 250px;
  height: 50px;
  padding: 0 25px;
  color: #979797;
  cursor: pointer;
}

.item-drawer > p {
  margin-left: 10px;
}

.item-drawer:hover {
  background: linear-gradient(
    90deg,
    #03dac5 -71.81%,
    rgba(3, 218, 197, 0.0001) 26.95%,
    rgba(3, 218, 197, 0.186725) 100%
  );
  mix-blend-mode: normal;
  opacity: 0.7;
  color: #03dac5;
}
</style>