<template>
  <v-data-table :headers="headers" :items="desserts" :items-per-page="6" class="elevation-1">
    <template v-slot:item.picture="{ item }">
      <img :src="item.picture" alt="colaborador" />
    </template>

    <template v-slot:item.name="{ item }">
      <router-link :to="`/user/${item.name}`">{{item.name}}</router-link>
    </template>

    <template v-slot:item.estado="{ item }">
      <v-icon :color="item.estado">{{item.carita}}</v-icon>
    </template>

    <template v-slot:item.aht="{ item }">
      <v-chip :color="getColor(item.aht)" dark>{{ item.aht }}</v-chip>
    </template>

    <template v-slot:item.vacum="{ item }">
      <v-chip :color="getColor(item.vacum)" dark>{{ item.vacum }}</v-chip>
    </template>

    <template v-slot:item.vconcr="{ item }">
      <v-chip :color="getColor(item.vconcr)" dark>{{ item.vconcr }}</v-chip>
    </template>

    <template v-slot:item.btn>
      <TableBtn />
    </template>
  </v-data-table>
</template>

<script>
import TableBtn from "../components/TableBtn";
export default {
  components: {
    TableBtn,
  },
  data() {
    return {
      headers: [
        {
          text: "Foto",
          value: "picture",
        },
        {
          text: "Nombre y Apellido",
          align: "start",
          sortable: false,
          value: "name",
        },
        { text: "Estado", value: "estado" },
        { text: "AHT", value: "aht" },
        { text: "V Acum.", value: "vacum" },
        { text: "V Concr.", value: "vconcr" },
        { text: "", value: "btn" },
      ],
      desserts: [
        {
          picture:
            "https://firebasestorage.googleapis.com/v0/b/coderplace-5d71e.appspot.com/o/imgPosts%2FCsOhUGLux5Pp78jjSwJR4G6EbD63%2Ftrabajador-1.png?alt=media&token=682355bf-2dae-407e-bf6d-f273fba2d1c2",
          name: "Juan Fajardo",
          estado: "#57d868",
          carita: "mdi-emoticon-happy",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
          btn: true,
        },
        {
          picture:
            "https://firebasestorage.googleapis.com/v0/b/coderplace-5d71e.appspot.com/o/imgPosts%2FCsOhUGLux5Pp78jjSwJR4G6EbD63%2Ftrabajador-2.png?alt=media&token=b1ae7504-8c80-447d-a5ed-d364cb768e40",
          name: "Jorge Valentin",
          estado: "#fde641",
          carita: "mdi-emoticon-neutral",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
          btn: "1%",
        },
        {
          picture:
            "https://firebasestorage.googleapis.com/v0/b/coderplace-5d71e.appspot.com/o/imgPosts%2FCsOhUGLux5Pp78jjSwJR4G6EbD63%2Ftrabajador-3.png?alt=media&token=a99c542c-9b0d-4831-a26e-b123e01907db",
          name: "Joshua Arnao",
          estado: "#fd3341",
          carita: "mdi-emoticon-sad",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
          btn: "7%",
        },
        {
          picture:
            "https://firebasestorage.googleapis.com/v0/b/coderplace-5d71e.appspot.com/o/imgPosts%2FCsOhUGLux5Pp78jjSwJR4G6EbD63%2Ftrabajador-4.png?alt=media&token=19c8db65-7ce4-448f-ba12-da42d8816cfb",
          name: "Alejandra López",
          estado: "#57d868",
          carita: "mdi-emoticon-happy",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
          btn: "8%",
        },
        {
          picture:
            "https://firebasestorage.googleapis.com/v0/b/coderplace-5d71e.appspot.com/o/imgPosts%2FCsOhUGLux5Pp78jjSwJR4G6EbD63%2Ftrabajador-5.png?alt=media&token=5852f48f-743f-4021-be13-26d4e8910724",
          name: "Amy Fernández",
          estado: "#57d868",
          carita: "mdi-emoticon-happy",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
          btn: "16%",
        },
        {
          picture:
            "https://firebasestorage.googleapis.com/v0/b/coderplace-5d71e.appspot.com/o/imgPosts%2FCsOhUGLux5Pp78jjSwJR4G6EbD63%2Ftrabajador-6.png?alt=media&token=6d21dce2-f02f-4a88-9b6a-8d2467228e98",
          name: "Alexa Wong",
          estado: "#57d868",
          carita: "mdi-emoticon-happy",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
          btn: "16%",
        },
      ],
    };
  },
  methods: {
    getColor(kpi) {
      if (kpi > 100) return "#57d868";
      else if (kpi > 50) return "#fde641";
      else return "#fd3341";
    },
    getRandom() {
      return Math.ceil(Math.random() * (150 - 10) + 10);
    },
  },
};
</script>

<style>
.v-data-table {
  text-align: center;
}

.v-data-table__wrapper img {
  margin-top: 6px;
  width: 40px;
  border-radius: 50px;
}
</style>