<template>
    <div>
        <p>This is a Cat
        <img :src="imageUrl">
    </div>
</template>

<script>
export default {
    data() {
        return{
            imageUrl:''
        }
    },

    created() {
        fetch('https://aws.random.cat/meow')
            .then(response => response.json())
            .then(data => this.imageUrl = data.file);
    }
}
</script>

<style scoped>
</style>