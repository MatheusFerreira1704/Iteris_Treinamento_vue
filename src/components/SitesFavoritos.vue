<template>
  <div class="sites-favoritos">
    <h2>Sites Favoritos</h2>
    <ul>
      <li v-for="sites of sitesFavoritos" :key="sites.id">
        <a href="sites.link">{{ sites.nome }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SitesFavoritos",
  data() {
    return {
      /*Arrei de Objetos*/
      sitesFavoritos: [],
    };
  },
  /*Consumindo a API*/
  created() {
    /*Isso é a API*/
    fetch("https://hackthon-decola.firebaseio.com/sites-favoritos.json")
      /*criando um pipe*/
      /*.json, função do JS que transforma em json.*/
      .then((resultado) => resultado.json())
      .then((json) => {
        this.sitesFavoritos = json;
      });
  },
};
</script>

<style scoped></style>>
