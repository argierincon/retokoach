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
  padding: 1.5% 3%;
  box-shadow: -2px 0px 4px rgba(0, 0, 0, 0.25), 0px 3px 4px rgba(0, 0, 0, 0.25);
}

.search > img {
  width: 8%;
  margin-right: 10px;
}

.search > input {
  outline: none;
}
</style>