<template>
    <div >Your Pokemon is {{name}}</div>
</template>

<script>
export default {
    data() {
        return{
            name:'',
            randomNumber: 1
        }
    },

    created() {
        this.randomNumber = Math.floor((Math.random() * 893) + 1);
        fetch('https://pokeapi.co/api/v2/pokemon-form/' + this.randomNumber)
            .then(response => response.json())
            .then(data => this.name = data.name);
    }
}
</script>

<style scoped>
</style>