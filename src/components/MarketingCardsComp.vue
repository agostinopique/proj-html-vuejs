<template>
    <div class="market-square">
        <div class="marketing-img">
            <img :src="tip.image" :alt="tip.title">
            <div class="overlay"></div>
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
    width: 410px;
    .marketing-img{
        width: 100%;
        position: relative;
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

.overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: .5s ease;
    background: rgb(248,95,17);
    background: linear-gradient(0deg, rgba(248,95,17,1) 0%, rgba(255,255,255,1) 70%);
}

.marketing-img:hover .overlay {
    opacity: 0.5;
}

</style>