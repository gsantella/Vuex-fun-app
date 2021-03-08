<template>
    <div>
        <watson-comp-1 />
        <div>My Links: <watson-comp-2 /></div>
        <watson-comp-3 text="Below Are Some Examples" />
        <div class="box"><watson-comp-4 /></div>
        <div class="box">Loading<watson-comp-5 /></div>
        <div class="box"><watson-comp-6 /></div>
        <div class="box"><watson-comp-7 /></div>
        <div class="box"><watson-comp-8 /></div>
        <div class="box"><watson-comp-9 text="Hello"/></div>
    </div>
</template>

<script>
import WatsonComp1 from './Watson/WatsonComp1.vue'
import WatsonComp2 from './Watson/WatsonComp2.vue'
import WatsonComp3 from './Watson/WatsonComp3.vue'
import WatsonComp4 from './Watson/WatsonComp4.vue'
import WatsonComp5 from './Watson/WatsonComp5.vue'
import WatsonComp6 from './Watson/WatsonComp6.vue'
import WatsonComp7 from './Watson/WatsonComp7.vue'
import WatsonComp8 from './Watson/WatsonComp8.vue'
import WatsonComp9 from './Watson/WatsonComp9.vue'
export default {
    
    components: {
        WatsonComp1,
        WatsonComp2,
        WatsonComp3,
        WatsonComp4,
        WatsonComp5,
        WatsonComp6,
        WatsonComp7,
        WatsonComp8,
        WatsonComp9
        
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