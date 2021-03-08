<template>
    <div>
        <h1>Clicker Game</h1>
        <button v-on:click="clicker">Click Me!</button>
        <p>{{ clicks }}</p>
    </div>
</template>


<script>
var clicker = 0

export default {
    data(){
        return{
            clicks:"0"
        }
    },
    methods:{
        clicker(){


            clicker = clicker + 1

            this.clicks = clicker
        }
    }
}
</script>
