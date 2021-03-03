<template>
  <div>
    <label>This is a button with sound</label>
    <br />
    <Button @click="playSound()">Sound Button</Button>
  </div>
</template>

<script>
export default {
  methods: {
    playSound() {
      var data = {
        bell: "http://soundbible.com/grab.php?id=2205&type=mp3",
      };
      var audio = new Audio(data.bell);
      audio.play();
    },
  },
};
</script>

<style scoped>
</style>