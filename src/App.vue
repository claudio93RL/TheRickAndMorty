<template>
  <div id="app">
    <ListaDeImagen />
  </div>
</template>

<script>
import ListaDeImagen from "./components/ListaDeImagen.vue";
export default {
  name: "App",
  components: {
    ListaDeImagen,
  },
};
</script>

<style>
body {
  background-image: url("./assets/cropped-RM_page-header_background1-3.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  height: 100%;
}
</style>
