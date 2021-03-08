<template>
  <div class="container">
    <h1>Background Image</h1>
    <p>Enter Image URL:</p>
    <div :style="{ backgroundImage: `url(${backgroundURL})` }">
      <input type="text" id="imageURL" v-model="imageURL" name="imageURL">
      <button @click="changeBackground">Submit</button>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      backgroundURL:""
    };
  },
  methods: {
    changeBackground() {

      var URL = document.querySelector("input[name=imageURL]").value
      this.backgroundURL = URL

    },
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
