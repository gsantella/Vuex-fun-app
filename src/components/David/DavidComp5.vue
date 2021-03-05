<template>
    <div>
        <h3>Random Programming Joke</h3>
        <p style="white-space:pre-line">{{ joke }}</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            joke:""
        }
    },
    created(){
        fetch("https://v2.jokeapi.dev/joke/Programming?format=json&blacklistFlags=nsfw%2Creligious%2Cpolitical%2Cracist%2Csexist%2Cexplicit&type=single", {
            "method": "GET",
            "headers": {
                "cookie": "__cfduid=d4ace96c01a14a25d52a6958256992b221614279288",
                "x-rapidapi-key": "7e24d54752msh24e9a1b20079146p1d69f8jsn321ba73fce0c",
                "x-rapidapi-host": "jokeapi.p.rapidapi.com"
            }
        })
        .then(response => {
            return response.json();
        })
        .then(json => {
            this.joke = json.joke
        })
        .catch(err => {
            console.error(err);
        });
    }
}
</script>