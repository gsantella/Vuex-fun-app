<template>
    <div v-bind:style="{backgroundColor: colorHex}">
        <p>This background color has the hex code {{ colorHex }}.</p>
        <button v-on:click="changeColor()">Change Color</button>
    </div>
</template>
<script>
export default {
    data(){
        return{
            colorHex:''
        }
    },
    created(){
        this.changeColor()
    },
    methods:{
        changeColor(){
            let red = Math.floor(Math.random()*128) + 128
            let green = Math.floor(Math.random()*128) + 128
            let blue = Math.floor(Math.random()*128) + 128
            red = red.toString(16)
            green = green.toString(16)
            blue = blue.toString(16)
            this.colorHex = '#' + red + green + blue
        }
    }
}
</script>