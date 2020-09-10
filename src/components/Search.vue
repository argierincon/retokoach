<template>
  <div class="search">
    <img src="../assets/img/search.png" alt="lupa" />
    <input type="text" placeholder="Buscar" />
  </div>
</template>

<style>
.search {
  display: flex;
  align-items: center;
  width: 300px;
  height: 45px;
  background: #ffffff !important;
  border-radius: 25px;
  padding: 1% 2%;
}

.search > img {
  width: 10%;
  margin-right: 10px;
}

.search > input {
  outline: none;
}
</style>