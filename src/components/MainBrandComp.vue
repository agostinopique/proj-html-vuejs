<template>
    <div class="ap-container">
        <h2>Trusted by Leading Organisations</h2>
        <div class="card-container">
            <BrandCard 
                v-for="(brandData, index) in improvements"
                :key="index"
                :brandData= "brandData"/>
        </div>
            <button id="hover-btn" class="main-btn">Read More Case Studies</button>
    </div>
</template>

<script>
import BrandCard from './BrandCard.vue';
import brandIncrease from '@/assets/script/brandIncrease';


export default {
    name: "MainBrandComp",
    components: { BrandCard },
    data(){
        return {
            improvements: brandIncrease
        }
    }
}
</script>

<style lang="scss" scoped>
.ap-container{
    display: flex;
    width: 70%;
    margin: 0 auto;
    margin-top: 200px;
    flex-direction: column;
    h2{
        font-size: 45px;
        font-weight: bold;
        text-align: center;
        margin-bottom: 50px;
    }
    .main-btn{
        align-self: center;
        margin-top: 60px;
        border: none;
        padding: 8px 25px;
        border-radius: 7px;
        background-color: #F85F11;
        color: white;
    }
}
.card-container{
    display: flex;
    justify-content: space-evenly;
}
</style>