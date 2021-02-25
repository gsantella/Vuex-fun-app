<template>
    <div><hr>
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
            .then(data => this.imageUrl = data.message);
    }
}
</script>

<style scoped>
    img { width: 64% }
</style>