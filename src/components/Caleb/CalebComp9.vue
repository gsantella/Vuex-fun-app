<template>
    <div>
        <p>Timer: {{clock}}</p>
    </div>
</template>

<script>
export default {
    data()
    {
        return{
            clock: 0
        }
    },
    created()
    {
       this.interval = setInterval(()=>this.upKeep(),1000);
    },
    methods:
    {
        upKeep: function(){
            this.clock = this.clock + 1;
        }
    }
}
</script>

<style scoped>
</style>