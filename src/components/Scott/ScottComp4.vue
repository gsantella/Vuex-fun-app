<template>
  <div :style="{ backgroundColor: backgroundcolor }">
    <button @click="start">New color</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      backgroundcolor: "#000000",
      color: [
        "#0000ff",
        "#00ffff",
        "#00ff00",
        "#ccff66",
        "#ff6600",
        "#ff3399",
        "#ff00ff",
        "#6666ff",
        "#ffffff",
        "#003300",
        "#660066",
      ],
    };
  },
  methods: {
    start() {
      this.backgroundcolor = this.color[Math.floor(Math.random() * 10)];
    },
  },
};
</script>

<style scoped>
</style>