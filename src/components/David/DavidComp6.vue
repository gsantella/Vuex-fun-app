<template>
    <div>
        <h3>"Love Calculator"</h3>
        <form v-on:submit="submitCalculation">
            <label for="name1">Your Name:</label>
            <input type="text" v-model="name1" required>
            <br>
            <label for="name2">Crush's Name</label>
            <input type="text" v-model="name2" required>
            <br>
            <button type="submit">Submit</button>
        </form>
        <p v-show="gotResults">You are {{ percent }}% compatible. {{ message }}</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            name1:"",
            name2:"",
            gotResults:false,
            percent:0,
            message:"",
            apiAddress:"https://love-calculator.p.rapidapi.com/getPercentage?"
        }
    },
    methods:{
        submitCalculation(e){
            e.preventDefault()
            if (this.name1 && this.name2){
                let address = this.apiAddress
                address += "fname=" + this.name1
                address += "&sname=" + this.name2
                fetch(address, {
                    "method": "GET",
                    "headers": {
                        "x-rapidapi-key": "7e24d54752msh24e9a1b20079146p1d69f8jsn321ba73fce0c",
                        "x-rapidapi-host": "love-calculator.p.rapidapi.com"
                    }
                })
                .then(response => {
                    return response.json();
                })
                .then(json => {
                    this.percent = json.percentage
                    this.message = json.result
                    this.gotResults = true
                })
                .catch(err => {
                    console.error(err);
                });
            }
        }
    }
}
</script>