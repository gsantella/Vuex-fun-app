  <template>
  <div>
    <p>Number of Clicks: {{ number }}</p>
    <button @click.prevent="addClick">Click Me</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0,
    };
  },

  methods: {
    addClick() {
      this.number = this.number + 1;
    },
  },
};
</script>

<style scoped>
</style>