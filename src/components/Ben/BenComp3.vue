<template>
  <div :style="{ backgroundColor: newcolor }" id="body">
    <button @click="start" id="colorButton">Change Color!</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newcolor: "#FFFFFF",
      color: [
        "#2C3AB5",
        "#FFFFFF",
        "#FA0808",
        "#FF06D9",
        "#06D5FF",
        "#37FF06",
        "#06CEFF",
        "#CEFF06",
        "#FF5906",
        "#6106FF",
        "#5C414D",
        "#95E8C0",
        "#B3BBBB",
        "#0A0A32",
        "#000000",
        "#BF5BBC",
        "#FF00F3",
        "#1A501C",
        "#F97500",
      ],
    };
  },
  methods: {
    start() {
      this.newcolor = this.color[Math.floor(Math.random() * 19)];
    },
  },
};
</script>

<style scoped>
#body {
height: 500px;
}
#colorButton{
margin-top: 10%;
}
</style>
