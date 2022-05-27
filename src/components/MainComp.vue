<template>
<div>
    <JumboComp />
    <CardComp
        v-for="(card, index) in cardElements"
        :key="`Card-${index}`"
        :cardElement="card" />
</div>
</template>

<script>
import JumboComp from './JumboComp.vue'
import CardComp from './CardComp.vue'
import cardElements from '@/assets/script/cardElements'

export default {
    name: 'MainComp',
    components: {
        JumboComp,
        CardComp
    },
    data(){
        return{
            cardElements: cardElements
        }
    }
}
</script>

<style lang="scss" scoped>

</style>