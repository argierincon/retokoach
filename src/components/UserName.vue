<template>
  <div class="user-name">
    <p>{{greeting}} {{userName}}</p>
  </div>
</template>

<script>
export default {
  name: "UserName",
  props: {
    userName: {
      type: String,
      default: "Jimena,",
    },
    greeting: {
      type: String,
      default: "Hola",
    },
  },
};
</script>

<style scoped>
.user-name {
  width: 700px;
  height: 50px;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  color: #2276bb;
  background: #fff;
  border-radius: 25px;
  padding: 10px 20px;
  box-shadow: -2px 0px 4px rgba(0, 0, 0, 0.25), 0px 3px 4px rgba(0, 0, 0, 0.25);
}
</style>