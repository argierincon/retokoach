<template>
  <p class="title-section">{{name}}</p>
</template>

<script>
export default {
  props: {
    name: String,
  }  
}
</script>

<style>
.title-section {
  margin-bottom: 3%;
  font-size: 28px;
  font-weight: bold;
  color: #ff7900;
}
</style>