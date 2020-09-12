<template>
  <div class="drawer">
    <div class="logo">
      <img src="../assets/img/koaching-logo.png" alt="koaching logo" />
    </div>
    <div class="user-data">
      <img src="../assets/img/user-one.png" alt="usuario logueado" />
      <p>Jimena Lozano</p>
    </div>
    <div>
      <ItemDrawer icon="mdi-home" item="Inicio" />
      <ItemDrawer icon="mdi-account-multiple" item="Seguimientos" />
      <ItemDrawer icon="mdi-bell" item="Notificaciones" />
      <ItemDrawer icon="mdi-account" item="Perfil" />
      <ItemDrawer icon="mdi-location-exit" item="Cerrar Sesión" />
    </div>
  </div>
</template>

<script>
import ItemDrawer from "../components/ItemDrawer";
export default {
  components: {
    ItemDrawer,
  },
};
</script>

<style>
.drawer {
  width: 250px;
  height: 100vh;
  background: #fff;
}

.logo {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 40px 0;
}

.logo > img {
  width: 100px;
  margin: auto;
}

.user-data {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #2276bb;
  font-weight: 700;
  margin-bottom: 30px;
}

.user-data > img {
  width: 150px;
  border-radius: 100px;
  margin-bottom: 30px;
}

.items-container {
  height: 50vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>