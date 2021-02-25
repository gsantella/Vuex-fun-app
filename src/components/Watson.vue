<template>
    <div>
        <watson-comp-1 />
        <watson-comp-3 text="Below Are Some Examples" />
        <div class="box"><watson-comp-4 /></div>
        <div class="box"><watson-comp-4 /></div>
    </div>
</template>

<script>
import WatsonComp1 from './Watson/WatsonComp1.vue'
import WatsonComp3 from './Watson/WatsonComp3.vue'
import WatsonComp4 from './Watson/WatsonComp4.vue'
export default {
    
    components: {
        WatsonComp1,
        WatsonComp3,
        WatsonComp4
        
    }

}
</script>

<style scoped>
    .box
    {
        width: 49%;
        border-style: solid;
        display: inline-block;
    }
</style>