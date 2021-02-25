<template>
    <div>
        <p>What is {{ question }}?</p>
        <input type="number" v-model="input">
        <Button v-on:click="submitAnswer">Submit</Button>
        <p v-show="right">Yes, that is correct</p>
        <p v-show="wrong">Sorry, that answer is incorrect.</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            question:"",
            answer:"",
            input:"",
            right:false,
            wrong:false
        }
    },
    created(){
        fetch("https://numbersapi.p.rapidapi.com/random/trivia?max=100&fragment=true&json=true", {
            "method": "GET",
            "headers": {
                "X-RapidAPI-Key": "7e24d54752msh24e9a1b20079146p1d69f8jsn321ba73fce0c",
                "X-RapidAPI-Host": "numbersapi.rapidapi.com"
            }
        })
        .then(response => {
            return response.json();
        })
        .then(json => {
            this.question = json.text;
            this.answer = json.number;
        })
        .catch(err => {
            console.error(err);
        });
    },
    methods:{
        submitAnswer(){
            if (this.input == this.answer){
                this.right = true
                this.wrong = false
            }
            else{
                this.wrong = true
                this.right = false
            }
        }
    }
}
</script>