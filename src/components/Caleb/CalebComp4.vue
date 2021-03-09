<template>
    <div>
        <p>Time for some API fun</p>
        <p>{{setup}}</p>
    </div>
</template>

<script>
export default {
    data()
    {
        return{
            setup: ""
        }
    },
    created()
    {
        fetch('https://official-joke-api.appspot.com/jokes/random').then(
            response=>response.json()
        ).then(
            data => this.setup = data.setup + " " + data.punchline
        );
    }
}
</script>

<style scoped>
</style>