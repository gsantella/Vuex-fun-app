<template>
    <div><hr>
        <button v-on:click="changeBackground">Change Background</button>
        <button v-on:click="reset">Reset</button>
    </div>
</template>

<script>
var red = true;
export default {
    data() {
        return{
        }
    },
    methods: {
        
        changeBackground() {
            if (red)
            {
                document.body.style.backgroundColor = "green";
                red = false;
            }
            else
            {
                document.body.style.backgroundColor = "red";
                red = true;
            }
            
        },

        reset() {
            document.body.style.backgroundColor = "white";
            red = true;
        }
    }

}
</script>


<style scoped>
</style>