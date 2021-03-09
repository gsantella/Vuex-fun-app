<template>
    <div>
        <button id="colorChanger" v-on:click ="color">Click to change the color</button>

    </div>
</template>

<script>
export default {
    data(){
        return{
            R:0,
            G:0,
            B:0
        }
    },
    methods:
    {
        color: function(){
            var btn = document.getElementById("colorChanger");
            this.R=Math.floor(Math.random() * (255 - 0 + 1) + 0);
            this.G=Math.floor(Math.random() * (255 - 0 + 1) + 0);
            this.B=Math.floor(Math.random() * (255 - 0 + 1) + 0);
            btn.style.backgroundColor= "rgb(" + this.R + "," + this.G + "," + this.B + ")";
        }
    }
}
</script>

<style scoped>
</style>