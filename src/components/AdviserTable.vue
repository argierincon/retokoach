<template>
  <v-data-table :headers="headers" :items="desserts" :items-per-page="5" class="elevation-1">
    <template v-slot:item.picture="{ item }">
      <img :src="item.picture" alt="colaborador" />
    </template>

    <template v-slot:item.name="{ item }">{{item.name}}</template>

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
  </v-data-table>
</template>

<script>
export default {
  components: {},
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
        { text: "Ventas Acum.", value: "vacum" },
        { text: "Ventas Concr.", value: "vconcr" },
      ],
      desserts: [
        {
          picture: "prueba",
          name: this.$route.params.name,
          estado: "#57d868",
          carita: "mdi-emoticon-happy",
          aht: this.getRandom(),
          vacum: this.getRandom(),
          vconcr: this.getRandom(),
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