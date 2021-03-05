<template>
    <div class="container">
        <h3>Random Fox</h3>
        <img v-bind:src="address" alt="Image of a fox">
        <br>
        <button v-on:click="newFox">New Fox</button>
    </div>
</template>
<script>
export default {
    data(){
        return{
            address:"https://randomfox.ca/images/1.jpg"
        }
    },
    created(){
        this.newFox()
    },
    methods:{
        newFox(){
            let randomNumber = Math.ceil(Math.random()*122)
            this.address = "https://randomfox.ca/images/" + randomNumber + ".jpg"
        }
    }
}
</script>
<style scoped>
img {
    width: 250px;
    height: auto;
}
</style>