<template>
    <div class="ap_card">
        <div v-if="cardIndex % 2" class="card-text-onLeft">
            <div class="card-logo">
                <span :style="{color: cardElement.color}" v-html="cardElement.logo"></span>
                <p class="type">{{cardElement.type}}</p>
            </div>
            <h2>{{cardElement.title}}</h2>
            <p>{{cardElement.text}}</p>
            <button id="hover-btn" class="card-btn">Get a Consultation</button>
        </div>
        <div class="card-img">
            <img :src="cardElement.image" :alt="cardElement.type">
        </div>
        <div v-if="!(cardIndex % 2)" class="card-text">
            <div class="card-logo">
                <span :style="{color: cardElement.color}" v-html="cardElement.logo"></span>
                <p class="type">{{cardElement.type}}</p>
            </div>
            <h2>{{cardElement.title}}</h2>
            <p>{{cardElement.text}}</p>
            <button id="hover-btn" class="card-btn">Get a Consultation</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardComp',
    props:{
        cardElement: Object,
        cardIndex: Number
    }
}
</script>
<style lang="scss" scoped>
.ap_card{
    width: 70%;
    margin: 0 auto;
    margin-bottom: 100px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.card-img{
    width: 50%;
}
.card-text-onLeft{
    width: 40%;
    padding-right: 60px;
    h2{
        font-size: 45px;
        font-weight: bold;
    }
    p{
        font-size: 20px;
        margin: 20px 0;
    }
    .type{
        margin-left: 10px;
        font-size: 15px;
    }
}
.card-text {   
    padding-left: 60px;
    width: 40%;
    h2{
        font-size: 45px;
        font-weight: bold;
    }
    p{
        font-size: 20px;
        margin: 20px 0;
    }
        margin-left: 10px;
    .type{
        margin-left: 10px;
        font-size: 15px;
    }
}
.card-logo{
    display: flex;
    align-items: center;
}
.card-btn{
    margin-top: 15px;
    border: none;
    padding: 10px 28px;
    border-radius: 7px;
    background-color: #F85F11;
    color: white;
    font-size: 16px;
}

.card-img {

    img{
        width: 80%;
    }
}

</style>