<template>
    <div>{{text}}</div>
</template>

<script>
export default {
    props: ["text"]
}
</script>

<style scoped>
    div {
        width: 100%;
        border-bottom-style: dashed;
    }
</style>