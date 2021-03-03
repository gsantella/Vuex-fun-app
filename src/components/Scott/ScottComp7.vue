<template>
  <div>
    <input id="results" type="text" />
    <button id="submit" @click.prevent="submit()">Submit</button>
    <p>You submitted "{{ text }}" to this text box via the input box</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: " ",
    };
  },
  methods: {
    submit() {
      this.input = document.getElementById("results").value;
    },
  },
};
</script>

<style scoped>
</style>