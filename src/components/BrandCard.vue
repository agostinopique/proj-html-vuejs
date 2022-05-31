<template>
    <div class="brand-card">
        <div class="brand-img">
            <img :src="brandData.image" :alt="brandData.brand">
            <div class="overlay"></div>
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
    width: 410px;
    .brand-img{
        width: 100%;
        margin-bottom: 15px;
        position: relative;
        img{
            width: 100%;
        }
    }
    .brand-description{

        p{
            font-size: 22px;
            margin-bottom: 30px;
        }
        .increase-data {
            font-size: 45px;
            font-weight: bold;
        }
        span {
            display: block;
        }
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

.brand-img:hover .overlay {
    opacity: 0.5;
}
</style>