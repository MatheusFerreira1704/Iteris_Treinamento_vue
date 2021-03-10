<template>
  <div class="contador">
    <h3>Contador: {{ i }}</h3>
    <button v-on:click="incrementar">
      <strong>+</strong>
    </button>
    <button v-on:click="decrementar"><strong>-</strong></button>
  </div>
</template>

<script>
export default {
  name: "Contador",
  data() {
    return {
      i: 0,
    };
  },
  methods: {
    incrementar() {
      this.i = this.i += 1;
    },
    decrementar() {
      this.i = this.i -= 1;
    },
  },
};
</script>

<style scoped></style>
