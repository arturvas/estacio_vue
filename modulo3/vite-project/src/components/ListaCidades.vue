<template>
  <div class="lista">
    <div class="card" v-for="cidade in cidades" :key="cidade.id">
      <div class="card-img"></div>
      <h3>{{ cidade.name }}</h3>
      <h4>{{ cidade.description }}</h4>
      <div class="temperatura">{{ cidade.temp }}º</div>
    </div>
  </div>
</template>

<script>
import "/assets/estilo.css";
import Cabecalho from "./components/Cabecalho.vue";

export default {
  components: { Cabecalho },
  data() {
    return {
      cidades: [
        {
          id: 8429,
          name: "Rio de Janeiro",
          description: "Ensolarado",
          icon: "01d",
          temp: "25",
        },
        {
          id: 8412,
          name: "Manaus",
          description: "Chuvas fortes",
          icon: "09d",
          temp: "25",
        },
        {
          id: 8454,
          name: "Brasília",
          description: "Ensolarado",
          icon: "10d",
          temp: "27.4",
        },
      ],
    };
  },
};
</script>
