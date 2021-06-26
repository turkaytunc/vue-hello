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
      this.$emit('closemodal');
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
  background-color: red;
  color: aliceblue;
}
</style>
