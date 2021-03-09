<template>
  <div>
    <p>Today is {{weekDays[day]}}</p>
  </div>
</template>

<script>
export default {
  data() {
        return{
            day: new Date().getDay(""), 
            weekDays: 
            [
              "Sunday",
              "Monday",
              "Tuesday",
              "Wednesday",
              "Thursday",
              "Friday",
              "Saturday"
            ]
        }
    }
    
}
</script>

<style scoped>
</style>