<template>
    <div>
        <h1>Date and Time</h1>
        <h1>{{ time }}</h1>
    </div>
</template>
<script>

export default {
    data(){
        return{
          time: ""
        }
    },
    created() {
                setInterval(this.getNow, 1000);
    },
    methods:{

    getNow: function() {
                const today = new Date();
                const date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
                const time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
                const dateTime = date +' '+ time;
                this.time = dateTime;
            }
    }
}
</script>
