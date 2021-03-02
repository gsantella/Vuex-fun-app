<template>
    <div><hr>
        <h1>Trivia</h1>
        <p>Trivia difficulty: {{trivia.results[0].difficulty}}</p>
        <p>{{trivia.results[0].question}}</p>
        <h7><b>{{trivia.results[0].correct_answer}}</b></h7>
    </div>
</template>

<script>
export default {
    data() {
        return{
            trivia: {}
        }
    },
    created() {
        fetch('https://opentdb.com/api.php?amount=1')
            .then(response => response.json())
            .then(data => this.trivia = data);
    }
}
</script>


<style scoped>
</style>