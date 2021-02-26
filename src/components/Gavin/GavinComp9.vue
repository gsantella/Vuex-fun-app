<template>
    <div><hr>
        <h1>Trivia</h1>
        <p>Trivia difficulty: {{trivia.difficulty}}</p>
        <p>{{trivia.question}}</p><br><br><br>
        <h7><b>{{trivia.correct_answer}}</b></h7>
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
            .then(data => this.trivia = data.results);
    }
}
</script>


<style scoped>
</style>