<template>
    <div>
        <p>A coin was flipped.</p>
        <p v-if="number%2 === 0">It was heads!</p>
        <p v-else>It was tails!</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            number: 0
        }
    },
    created(){
        let randomNumber = Math.random()*10
        this.number = Math.ceil(randomNumber)
    }
}
</script>