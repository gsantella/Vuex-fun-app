<template>
    <div><hr>
        <h1>Jokes</h1>
        <h3>Joke type: {{joke.type}}</h3>
        <h3>{{joke.setup}}</h3>
        <h7><b>{{joke.punchline}}</b></h7>
    </div>
</template>

<script>
export default {
    data() {
        return{
            joke: {}
        }
    },
    created() {
        fetch('https://official-joke-api.appspot.com/random_joke')
            .then(response => response.json())
            .then(data => this.joke = data);
    }
}
</script>


<style scoped>
</style>