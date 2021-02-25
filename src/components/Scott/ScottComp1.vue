<template>
  <div>
    <p>{{ name }}</p>
  </div>
</template>

<script>
export default {
  props: ["id"],

  data() {
    return {
      name: "test",
    };
  },

  created() {
    fetch(`https://anapioficeandfire.com/api/houses/${this.id}`)
      .then((response) => response.json())
      .then((data) => (this.name = data.name));
  },
};
</script>

<style scoped>
</style>