<template>
    <div><hr>
        <p>ISS current latitude: {{latitude}}</p>
    </div>
</template>

<script>
export default {
    data() {
        return{
            latitude:''
        }
    },

    created() {
        fetch('https://api.wheretheiss.at/v1/satellites/25544')
            .then(response => response.json())
            .then(data => this.latitude = data.latitude);
    }
}
</script>


<style scoped>
</style>