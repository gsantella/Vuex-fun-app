<template>
    <div>
        <p>This is a Dog>
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
        fetch('https://dog.ceo/api/breeds/image/random')
            .then(response => response.json())
            .then(data => this.imageUrl = data.file);
    }
}
</script>

<style scoped>
</style>