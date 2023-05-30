<template>
  <div>
    <h1>{{ title }}</h1>
    <Modal :header="header" :array="array" theme="sale" />
  </div>
</template>

<script>
import Modal from "./components/Modal";

export default {
  name: "App",
  components: { Modal },
  data() {
    return {
      title: "My First Vue App",
      header: "Sign up for a giveaway!",
      array: ["apple", 4],
    };
  },

  methods: {
    handleClick() {
      this.$refs.name.classList.add("active");
      this.$refs.name.focus();
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  border-bottom: 2px solid black;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
