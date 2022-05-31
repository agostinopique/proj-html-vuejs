<template>
    <div class="market-square">
        <div class="marketing-img">
            <img :src="tip.image" :alt="tip.title">
        </div>
        <p>{{tip.text}}</p>
    </div>
</template>

<script>

export default {
    name: 'MarketingCardsComp',
    props: {
        tip: Object
    }
}
</script>

<style lang="scss" scoped>
.market-square{
        width: 550px;
        .marketing-img{
            width: 100%;
            img{
                width: 100%;
            }
        }
        p{
            font-size: 30px;
            margin-top: 15px;
            padding-right: 30px;
        }
    }
</style>