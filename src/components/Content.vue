<template>
  <div class="home">
    <h1>Hello in my Home Page</h1>
  </div>
</template> 
<script>
export default {
  name: "Content",
  data() {
    return {
      testMessage: "",
      show: false,
    };
  },
};
</script>
<style>
button {
  background-color: #41b883;
  border: none;
  color: white;
  padding: 20px;
  margin: 0 20px;
  text-align: center;
  display: inline-block;
  font-size: 16px;
  cursor: pointer;
  border-radius: 12px;
}
.home {
  text-align: center;
  margin-bottom: 50px;
}
</style>