<template>
    <div>
        <h3>Robot Generator</h3>
        <img v-bind:src="robotPicLink" alt="The pic for the text you entered.">
        <form v-on:submit="getLink">
            <label for="input">Enter any text here:</label>
            <input type="text" v-model="input">
            <button type="submit">Get a Robot</button>
        </form>
    </div>
</template>
<script>
export default {
    data(){
        return{
            input:"",
            robotPicLink:"https://robohash.org/sample"
        }
    },
    methods:{
        getLink(e){
            e.preventDefault()
            this.robotPicLink = "https://robohash.org/" + this.input
        }
    }
}
</script>