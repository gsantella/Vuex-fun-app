<template>
    <div>
        <div>Text: {{text}}</div>
        <div>Morse Code: <a :href="morse">Link since cors needs to be disabled for the fetch</a></div>
    </div>
</template>

<script>
export default {
    props: ["text"],
    data() {
        return{
            morse: ''
        }
    },

    created() {
        this.morse = `https://api.funtranslations.com/translate/morse.json?text=${this.text}`
    }
}
</script>

<style scoped>
</style>