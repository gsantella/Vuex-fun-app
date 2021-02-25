<template>
    <div><hr>
        <input id="input1" type="text">
        <p>You entered {{text}}</p>
        <button id="btn1" v-on:click="putInBox">Click</button>
    </div>
</template>

<script>
export default {
    data() {
        return{
            text:''
        }
    },
    methods: {
        putInBox() {
            this.text = document.getElementById('input1').value;
        }
    }
    

    
}

</script>

<style scoped>

</style>