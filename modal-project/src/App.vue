<template>
  <div>
    <h1>{{ title }}</h1>
    <p>Welcome...</p>
    <div v-if="showModal">
      <Modal @close="toggleModal">
        <h1>WWWEEWEWOJ YES BOYS!</h1>
        <p>OWA OWA OWA AWWWOOOOOGAAA!</p>
        <template v-slot:links>
          <a href="#">EEEEEEEE</a>
          <a href="#">AAA</a>
        </template>
      </Modal>
    </div>
    <button @click="toggleModal">Open Modal</button>
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
      showModal: false,
    };
  },

  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
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
