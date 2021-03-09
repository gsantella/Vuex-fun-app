<template>
  <div>
    <p>A little bit of random number gereration never hurts</p>
    <button v-on:click="random">Click here</button>
    <div>
      {{ number }}
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            number: 0
        }
    },
  methods: {
    random: function () {
      this.number = Math.random();
    },
  },
};
</script>

<style scoped>
</style>