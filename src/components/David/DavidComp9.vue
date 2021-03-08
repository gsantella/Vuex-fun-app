<template>
    <div>
        <form v-on:submit="sayThanks" v-show="needName">
            <label for="nameField">Please enter your name here</label>
            <input type="text" v-model="nameField">
            <button type="submit">Submit</button>
        </form>
        <p v-show="haveName">Thank you for looking at my page, {{ name }}.</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            nameField:"",
            name:"",
            needName:true,
            haveName:false
        }
    },
    methods:{
        sayThanks(e){
            e.preventDefault()
            this.name = this.nameField;
            this.needName = false;
            this.haveName = true;
        }
    }
}
</script>