<template>
    <div><hr>
        <h2>Click the mole<h2>
        <p>Total clicks: {{totalClicks}}</p>
        <button v-on:click="add"><img src="./mole.jpg" widht="300" height="300"></button>
    </div>
</template>

<script>


export default {
    data() {
        return{
            totalClicks:0
        }
    },
    methods: {
        add() {
            this.totalClicks+=1;
        }
    }

}
</script>


<style scoped>
</style>