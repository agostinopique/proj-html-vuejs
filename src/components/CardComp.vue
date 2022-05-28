<template>
    <div class="ap_card container">
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
    margin-bottom: 40px;
    display: flex;
    align-items: center;
}
.card-text,
.card-img{
    width: 50%;
    // min-height: 400px;
}
.card-text-onLeft{
    width: 50%;
    // min-height: 400px;
    padding: 50px 250px 0 0;
}
.card-text {
    padding: 50px 100px 0 150px;
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
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}

</style>