<template>
  <div>
    <label>This input box submits with the release of the enter key</label>
    <br />
    <input @keyup.enter="greet()" />
  </div>
</template>

<script>
export default {
  methods: {
    greet: function () {
      alert("You Submit using the enter button");
    },
  },
};
</script>

<style scoped>
</style>
