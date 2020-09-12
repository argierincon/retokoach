<template>
  <section class="box">
    <div class="header"></div>
    <div class="container-items">
      <slot />
    </div>
  </section>
</template>

<style scoped>
.box {
  width: 100%;
  height: 100vh;
}

.header {
  background: linear-gradient(90deg, #03dac5 0%, #08e7d1 49.48%, #8ae5d5 100%);
  height: 62px;
}

.container-items {
  padding: 4% 0;
  background: #f5f6f9;
}
</style>