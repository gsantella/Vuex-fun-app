<template>
    <div>
        <Button v-on:click="rollDie">Roll Die</Button>
        <p>{{ result }}</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            result:''
        }
    },
    methods:{
        rollDie(){
            let randomNumber = Math.random()*6
            this.result = Math.ceil(randomNumber)
        }
    }
}
</script>