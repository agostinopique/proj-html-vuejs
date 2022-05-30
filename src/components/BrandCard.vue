<template>
    <div class="brand-card">
        <div class="brand-img">
            <img :src="brandData.image" :alt="brandData.brand">
        </div>
        <div class="brand-description">
            <p>{{brandData.text}}</p>
            <span class="increase-data">{{brandData.percentage}}</span>
            <span>{{brandData.improvement}}</span>
        </div>
    </div>
</template>

<script>

export default {
    name: 'BrandCard',
    props:{
        brandData: Object
    }
}
</script>

<style lang="scss" scoped>
.brand-card {
    width: 330px;
    .brand-img{
        width: 100%;
        margin-bottom: 15px;
        img{
            width: 100%;
        }
    }
    .brand-description{

        p{
            font-size: 28px;
            margin-bottom: 30px;
        }
        .increase-data {
            font-size: 40px;
            font-weight: bold;
        }
        span {
            display: block;
        }
    }
}
</style>