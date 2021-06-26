<template>
  <div class="modal-container" @click.self="closeModal">
    <div class="modal-content">
      <p>Hello {{ msg }}</p>
      <button @click="closeModal">&times;</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Modal',
  props: {
    msg: String,
  },

  methods: {
    closeModal() {
      this.$emit('close-modal');
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.modal-container {
  display: flex;
  background-color: rgba(0, 0, 0, 0.5);
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  position: absolute;
  width: 100%;
  height: 100%;
}
.modal-content {
  background-color: #ddd;
  color: black;
  width: clamp(20rem, calc(100vw - 10rem), 50vw);
  height: clamp(20rem, calc(100vh - 20rem), 50vh);
  border-radius: 0.2rem;
  display: flex;
  position: relative;
  padding: 1rem;
  justify-content: center;
  align-items: center;
  box-shadow: 1px 1px 5px #333, -1px -1px 5px #333;
}

.modal-content button {
  font-size: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 1.5rem;
  background-color: transparent;
  text-align: center;
  border: none;
  cursor: pointer;
  position: absolute;
  right: 0.6rem;
  top: 0.1rem;
}

.modal-content button:hover {
  color: #555;
}
</style>
