<template>
  <h1>
    Hello
    {{ msg }}
    <input type="text" ref="vueInput" @change="handleChange" />
    <button @click="handleClick">Click Here</button>
  </h1>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },

  methods: {
    handleClick() {
      console.log(this.$.refs.vueInput.value);
    },
    handleChange(e) {
      console.log(e.target.value);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px 0 0;
  color: red;
}
</style>
