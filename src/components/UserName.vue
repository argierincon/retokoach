<template>
  <div class="user-name">
    <p>Hola {{userName}}</p>
  </div>
</template>

<script>
export default {
  name: "UserName",
  props: {
    userName: {
      type: String,
      default: "Jimena",
    },
  },
};
</script>

<style scoped>
.user-name {
  width: 40%;
  height: 50px;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  color: #2276bb;
  background: #fff;
  border-radius: 25px;
  padding: 0.9% 2%;
  margin: 3% 0 3% 5%;
}

/* p {
  font-family: Roboto;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 28px;
  color: #2276bb;
} */
</style>