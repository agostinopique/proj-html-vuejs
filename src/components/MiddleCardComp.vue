<template>
    <div class="ap_card">
        <div class="card-text">
            <h2>We Boost Our Clients' Bottom Line by Optimizing Their Growth Potential.</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus ad eius! Lorem ipsum dolor sit amet consectetur</p>
            <button id="hover-btn" class="card-btn">Why Work With Us</button>
        </div>
        <div class="card-img">
            <img src="../assets/img/we-boost-our-clients-600x549.jpg" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'MiddleCardComp'
}
</script>

<style lang="scss" scoped>

.ap_card{
    width: 70%;
    margin: 0 auto;
    margin-bottom: 70px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.card-text{
    width: 50%;
}

.card-img{
    width: 50%;
}
.card-text {
    padding-right: 250px;
    h2 {
        font-size: 40px;
        font-weight: bold;
    }
    p{
        font-size: 18px;
        font-weight: lighter;
        margin: 20px 0;
    }
}
.card-btn{
    margin-top: 15px;
    border: none;
    padding: 10px 28px;
    border-radius: 7px;
    background-color: #F85F11;
    color: white;
}

.card-img {

    img{
        width: 90%;
        height: 90%;
        object-fit: cover;
    }
}
</style>