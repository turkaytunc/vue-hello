<template>
  <Navbar />
  <div v-if="showModal"><Modal msg="vue" @close-modal="toggleModal" /></div>
  <button @click="toggleModal">Show Modal</button>
</template>

<script>
import Modal from './components/Modal.vue';
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    Modal,
    Navbar,
  },
  data() {
    return {
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  vertical-align: baseline;
  padding: 0;
}
body {
  scroll-behavior: smooth;
  position: relative;
}
</style>
