<template>
    <div class="center-main">
        <h2>Some Brands We Work With</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing!</p>
        <div class="brand-logos">
            <img v-for="(logo, index) in brandLogos" :key="`logo-${index}`"
            :src="logo.image" :alt="logo.title">
        </div>
    </div>
</template>

<script>
import brandLogos from '../assets/script/brandLogos'

export default {
    name: "PartBrandComp",
    data(){
        return{
            brandLogos : brandLogos
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';
.center-main{
    text-align: center;
    width: 70%;
    margin: 0 auto;
    margin-top: 150px;
    h2{
        font-weight: bold;
        font-size: 40px;
    }
    p{
        font-size: 20px;
        color: rgb(140, 137, 137);
    }

    .brand-logos{
        @include dFlexBetween;
        margin-top: 30px;
        img{
            width: 12%; 
        }
    }

}

</style>