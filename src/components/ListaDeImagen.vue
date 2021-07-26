<template>
  <div>
    <h1 class="col-5 mx-auto text-success">Personajes The Rick and Morty</h1>
    <div v-for="item in dataApi" :key="item.id">
      <img :src="item.image" alt="" />
      <h3 class="text-success">{{ item.name }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dataApi: [],
    };
  },
  methods: {
    async consumirApi() {
      try {
        const data = await fetch("https://rickandmortyapi.com/api/character");
        const respuesta = await data.json();
        this.dataApi = respuesta.results;
      } catch (error) {
        console.log(error);
      }
    },
  },
  created() {
    this.consumirApi();
  },
};
</script>

<style>
body {
  color: white;
}
img {
  width: 100px;
  border-radius: 100%;
  margin: 1rem;
}
h3 {
  display: inline-block;
}
</style>