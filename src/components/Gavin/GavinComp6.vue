<template>
    <div><hr>
        <p>Double the number: {{number}}</p>
        <button v-on:click="double">Double</button>
    </div>
</template>

<script>
export default {
    data() {
        return{
            number:1
        }
    },
    methods: {
        double() {
            this.number *= 2;
        }
    }

}
</script>


<style scoped>
</style>