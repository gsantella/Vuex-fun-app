<template>
    <div>
        <!-- Our New Components -->
        <RandomColor />
        <RandomColor />
        <NewComponent />
        <Counter />
        <Counter />
        <Counter />
        <Counter />
        <Hidden />
        <Counter />
        <HappySad />
        <StarWars character="8" />
        <StarWars character="9" />
        <StarWars character="2" />
        <RandomCat />
        <RandomCat />
        <RandomCat />
    </div>
</template>

<script>
import RandomColor from './Demo/RandomColor.vue'
import NewComponent from './Demo/NewComponent.vue'
import RandomCat from './Demo/RandomCat.vue'
import StarWars from './Demo/StarWars.vue'
import HappySad from './Demo/HappySad.vue'
import Counter from './Demo/Counter.vue'
import Hidden from './Demo/Hidden.vue'

export default {
    
    components: {
        RandomColor,
        NewComponent,
        RandomCat,
        StarWars,
        HappySad,
        Counter,
        Hidden
    }

}
</script>

<style scoped>

</style>