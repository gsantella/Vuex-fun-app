<template>
    <div><hr>
        <p>{{word}}</p>
    </div>
</template>

<script>
export default {
    data() {
        return{
            word:''
        }
    },
    created() {
        this.word= 'Hello World';
    }
}
</script>

<style scoped>

</style>