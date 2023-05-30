<template>
  <div>
    <h1>{{ title }}</h1>
    <Modal />
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
