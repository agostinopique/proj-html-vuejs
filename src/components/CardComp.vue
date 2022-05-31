<template>
    <div class="ap_card">
        <div v-if="cardIndex % 2" class="card-text-onLeft">
            <p>{{cardElement.type}}</p>
            <h2>{{cardElement.title}}</h2>
            <p>{{cardElement.text}}</p>
            <button class="card-btn">Get a Consultation</button>
        </div>
        <div class="card-img">
            <img :src="cardElement.image" :alt="cardElement.type">
        </div>
        <div v-if="!(cardIndex % 2)" class="card-text">
            <p>{{cardElement.type}}</p>
            <h2>{{cardElement.title}}</h2>
            <p>{{cardElement.text}}</p>
            <button class="card-btn">Get a Consultation</button>
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
    margin-bottom: 40px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.card-img{
    width: 50%;
}
.card-text-onLeft{
    width: 20%;
    // padding: 50px 250px 0 0;
    h2{
        font-size: 40px;
        font-weight: bold;
    }
}
.card-text {
    // padding: 50px 0 0 250px;
    width: 20%;
    h2{
        font-size: 40px;
        font-weight: bold;
    }
}
.card-btn{
    margin-top: 15px;
    border: none;
    padding: 8px 25px;
    border-radius: 7px;
    background-color: #F85F11;
    color: white;
}

.card-img {

    img{
        width: 80%;
    }
}

</style>