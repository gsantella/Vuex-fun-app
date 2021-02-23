<template>
  <div class="hello">
    <div class="container">
      <div class="">
        <div class="col-md-12">
          <div class="card">
            <div class="card-body">
              <h1>Hello Javascript!</h1>

            </div>
            
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  data(){
    return{
      stateData:''
    }
  },

  mounted(){
    this.stateData = this.$store.getters.getMessage
  },

  components: {
   
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
