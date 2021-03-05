<template>
    <div>
        <iframe :src="youtubeUrl"/>
    </div>
</template>

<script>
export default {
    data() {
        return{
            youtubeUrl:'https://www.youtube.com/embed/UgHKb_7884o'
        }
    },
}
</script>

<style scoped>
</style>