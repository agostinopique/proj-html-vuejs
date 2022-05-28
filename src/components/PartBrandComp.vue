<template>
    <div class="container center-main">
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

.center-main{
    text-align: center;
    h2{
        font-weight: bold;
        font-size: 35px;
    }
    p{
        color: rgb(177, 175, 175);
        font-size: 16px;
    }

    .brand-logos{
        display: flex;
        justify-content: space-between;
        margin-top: 30px;
        img{
            width: 10%; 
        }
    }

}

</style>