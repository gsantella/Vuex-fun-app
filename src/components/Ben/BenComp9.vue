<template>
    <div>
        <h1>Pound to Kilo</h1>
        <input type="text" name="pound">
        <button v-on:click="poundToKilo">Click Me!</button>
        <p>kg: {{ kiloOutput }}</p>
        <br>
        <h1>Kilo to Pound</h1>
        <input type="text" name="kilo">
        <button v-on:click="kiloToPound">Click Me!</button>
        <p>lb: {{ poundOutput }}</p>
    </div>
</template>


<script>

export default {
    data(){
        return{
          poundOutput:"0",
          kiloOutput:"0"
        }
    },
    methods:{
        poundToKilo(){

          var pound = document.querySelector("input[name=pound]").value
          pound = pound * 0.453592
          this.kiloOutput = pound

        },
        kiloToPound(){

          var kilo = document.querySelector("input[name=kilo]").value
          kilo = kilo * 2.20462
          this.poundOutput = kilo
        }
    }
}
</script>
