<template>
  <div class="teste-eventos">
    <h2>Teste Evento</h2>
    <!--Intercolação, monstra a variavél que está dentro.-->
    <!-- v-on é a direiva que de interação com usuário, pode ner substituido pelo ( @ )-->
    <p v-on:click="deixarMaiscula">{{ mensagem }}</p>

    {{ 1 + 1 }}
  </div>
</template>

<script>
export default {
  name: "TesteEvento",
  data() {
    return {
      mensagem: "Pernambuco meu país.",
    };
  },
  /*Função de deixar testo maisculo*/
  methods: {
    /*A mensagem vai ficar maiscula quando receber um click.*/
    deixarMaiscula() {
      this.mensagem = this.mensagem.toUpperCase();
    },
  },
};
</script>

<style scoped></style>