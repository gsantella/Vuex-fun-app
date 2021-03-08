<template>
    <div>
        <h1>Alert Popup Sound</h1>
        <button v-on:click="playSound">Click Me!</button>
        <br>
        <br>
        <button v-on:click="playMusic">Play Song!</button>
    </div>
</template>


<script>

var beepSound = { soundurl : 'http://codeskulptor-demos.commondatastorage.googleapis.com/GalaxyInvaders/pause.wav'}
var musicSound = {soundurl : 'http://codeskulptor-demos.commondatastorage.googleapis.com/GalaxyInvaders/theme_01.mp3'}
export default {
    data(){
        return{

        }
    },
    methods:{
        playSound(){


        var audio = new Audio(beepSound.soundurl);
        audio.play();
        alert("Beep! You clicked the button!");


        },
        playMusic(){

            var song = new Audio(musicSound.soundurl);
            song.play();
            alert("Now playing Galaxy Invaders Theme!");
        }
    }
}
</script>
