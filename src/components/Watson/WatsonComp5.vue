<template>
    <div>{{text}}</div>
</template>

<script>
export default {
    data() {
        return{
            text: "."
        }
    },
    created() {
    this.interval = setInterval(() => this.loading(), 750);
    },
    methods:
    {
        loading()
        {
            if (this.text == "...")
            {
                this.text = "."
            }
            else
            {
                this.text = this.text + "."
            }
        }
    }
}
</script>

<style scoped>
    div {
        display: inline;
    }
</style>