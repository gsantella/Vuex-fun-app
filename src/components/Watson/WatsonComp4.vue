<template>
    <div>{{time}}</div>
</template>

<script>
export default {
    data() {
        return{
            time: new Date().toLocaleTimeString()
        }
    },
    created() {
    this.interval = setInterval(() => this.updateTime(), 1000);
    },
    methods:
    {
        updateTime()
        {
            this.time = new Date().toLocaleTimeString();
        }
    }
}
</script>

<style scoped>
</style>