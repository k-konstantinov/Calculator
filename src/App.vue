<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Header />
  <component v-bind:is="currentPage"></component>
  <div class="btn-center">
    <button v-on:click="uploadPage('calculator')">Load Calculator</button>
    <button v-on:click="uploadPage('content')">Load Home</button>
  </div>
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import Calculator from "./components/Calculator.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    content: Content,
    calculator: Calculator,
    Footer,
  },
  data() {
    return { currentPage: "content" };
  },
  methods: {
    uploadPage(item) {
      this.currentPage = item;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
body {
  color: #35495e;
}
header {
  background: #41b883;
  color: white;
}
.btn-center{
  text-align: center;
}
.btn-center button{
  margin: 0 10px;
}
footer {
  margin-top: 50px;
  background: #35495e;
  color: white;
}
</style>
