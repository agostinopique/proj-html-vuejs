<template>
    <div class="award-card">
        <img :style="{filter: award.color}" :src="award.image" alt="">
        <p>{{award.text}}</p>
        <p>{{award.year}}</p>
    </div>
</template>

<script>
export default {
    name: 'AwardComp',
    props:{
        award: Object
    }
}
</script>

<style lang="scss" scoped>
.award-card{
    margin-top: 50px;
    img{
        width: 50%;
        margin-bottom: 20px;
    }
}
</style>