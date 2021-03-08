<template>
    <div>
        <h3>Weather In Altoona</h3>
        <p>{{ weather }}</p>
        <p>Temperature: {{ temp }} F</p>
    </div>
</template>
<script>
export default {
    data(){
        return{
            weather:"",
            temp:""
        }
    },
    created(){
        fetch("http://api.openweathermap.org/data/2.5/weather?q=Altoona,USA&APPID=08eacbf5e985015e3639427d29127a3b", {
            "method": "GET",

        })
        .then(response => {
            return response.json();
        })
        .then(json => {
            this.weather = json.weather[0].main

            var temperature = json.main.temp

            temperature = (temperature - 273.15) * 9/5 + 32
            this.temp = temperature
        })
        .catch(err => {
            console.error(err);
        });
    }
}
</script>
