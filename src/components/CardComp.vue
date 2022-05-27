<template>
    <div class="container d-flex">
        <div v-if="!cardElement.onRight" class="card-text-onLeft debug-class">
            <p>{{cardElement.type}}</p>
            <h2>{{cardElement.title}}</h2>
            <p>{{cardElement.text}}</p>
            <button class="card-btn">Get a Consultation</button>
        </div>
        <div class="card-img debug-class">IMMAGINE</div>
        <div v-if="cardElement.onRight" class="card-text debug-class">
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
        cardElement: Object
    }
}
</script>

<style lang="scss" scoped>
.debug-class{
    border: 1px solid black;
}
.card-text,
.card-img{
    width: 50%;
    min-height: 400px;
}
.card-text-onLeft{
    width: 50%;
    min-height: 400px;
    padding: 50px 100px 0  230px ;
}
.card-text {
    padding: 50px 250px 0 50px;
}
.card-btn{
    margin-top: 15px;
    border: none;
    padding: 8px 25px;
    border-radius: 7px;
    background-color: #F85F11;
    color: white;
}

</style>