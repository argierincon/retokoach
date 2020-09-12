<template>
  <div class="custom-btn">
    <img src="../assets/img/excel.png" alt="excel icon" />
    <button>Generar Reporte</button>
  </div>
</template>

<style>
.custom-btn {
  display: flex;
  align-items: center;
  height: 45px;
  width: 200px;
  padding: 12px;
  background: linear-gradient(0deg, #ff7900, #ff7900);
  border-radius: 25px;
  margin-right: 4%;
  cursor: pointer;
  color: #fff;
  box-shadow: -2px 0px 4px rgba(0, 0, 0, 0.25), 0px 3px 4px rgba(0, 0, 0, 0.25);
}

.custom-btn:hover {
  box-shadow: inset 0px 3px 4px rgba(0, 0, 0, 0.25),
    inset 6px 2px 4px rgba(0, 0, 0, 0.25), inset 2px 4px 4px rgba(0, 0, 0, 0.28);
}

.custom-btn > img {
  width: 30px;
  height: 30px;
  margin-right: 8px;
}

.custom-btn > button {
  outline: none;
}
</style>
