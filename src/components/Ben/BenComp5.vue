<template>
    <div>
        <h1>USD to Euro</h1>
        <input type="text" name="USD">
        <button v-on:click="USDToEuro">Click Me!</button>
        <p>€ {{ euroOutput }}</p>
        <br>
        <h1>Euro to USD</h1>
        <input type="text" name="Euro">
        <button v-on:click="EuroToUSD">Click Me!</button>
        <p>$ {{ USDOutput }}</p>
    </div>
</template>


<script>

export default {
    data(){
        return{
          euroOutput:"0",
          USDOutput:"0"
        }
    },
    methods:{
        USDToEuro(){

          var USD = document.querySelector("input[name=USD]").value
          USD = USD * 0.83
          this.euroOutput = USD

        },
        EuroToUSD(){

          var Euro = document.querySelector("input[name=Euro]").value
          Euro = Euro * 1.21
          this.USDOutput = Euro
        }
    }
}
</script>
