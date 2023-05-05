<script>
export default {
  data: () => ({
    contador: 0,
  }),
  methods: {
    saludar() {
      console.log("Hola");
    },
    incrementar() {
      this.contador++;
    },
    disminuir() {
      this.contador--;
    },
    resetear() {
      this.contador = 0;
    },
  },
};
</script>

<template>
  <div class="container">
    <img src="./assets/logo.svg" alt="logo vue" width="125" height="125" />
    <small>
      <h1>Hola mundo desde Vue.js 3</h1>
    </small>
    <hr />

    <h2>Counter: {{ contador }}</h2>
    <button @click="incrementar">+1</button>
    <button @click="disminuir">-1</button>
    <button @click="resetear">RESET</button>
  </div>
</template>

<!-- El scoped le da el style solo al archivo este (no a todos los H1, por ej) -->
<style scoped>
/* @import "./assets/base.css";  SE USA SI NO SE IMPORTA EL .css EN EL HTML*/
.container {
  text-align: center;
}
small {
  color: #666;
}
h1 {
  font-weight: bolder;
}
h2 {
  font-size: 2.5rem;
}
button {
  cursor: pointer;
  font-size: 1.5rem;
  margin: 0 0.5rem;
}
</style>
