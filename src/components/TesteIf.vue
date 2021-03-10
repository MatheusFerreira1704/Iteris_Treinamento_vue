<template>
  <div class="teste-if">
    <!-- Diretiva (v-if), deu poder ao HTML de realizar tomada de decisões. 
  Também tem a opção de (v-if-else e v-else) -->

    <h1 v-if="podeVer">Teste igual a true</h1>
    <h1 v-else>Teste igual a false</h1>
  </div>
</template>

<script>
export default {
  name: "TesteIf",
  data() {
    return {
      /* Se podeVer = false, vai exibir titulo do v-else.*/
      podeVer: true,
    };
  },
};
</script>

<style scoped></style>>
