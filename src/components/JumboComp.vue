<template>
    <div class="jumbotron">
            <div class="jumbo-demo">
                <i class="bi bi-folder-symlink-fill" style="font-size: 1.5rem;"></i>
                <p>Demos</p>
            </div>
            <div class="jumbo-price">
                <div class="price-text">
                    <i class="bi bi-currency-dollar" style="font-size: 13px;"></i>
                    <p>39</p>
                </div>
                <p>On Sale</p>
            </div>
        <div class="container d-flex">
            <div class="jumbo-text">
                <h1>Unlock Your Online <br>
                    Growth Potential</h1>
                <p>Online marketing to secure customer retention, <br> leads, and sales. We focus on the bigger picture.</p>
                <button class="jumbo-btn">Our Services <i class="bi bi-arrow-right-short"></i></button>
            </div>
            <div class="jumbo-right">
                <div class="jumbo-form">

                    <div class="profile-info">
                        <img src="../assets/img/marketing-consultant-expert.jpg" alt="consultant-expert">
                    </div>
                </div>
                <div></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "JumboComp"
}
</script>

<style lang="scss" scoped>
.debug-class {
    border: 1px solid black;
    height: 100%;
}

.jumbotron {
    height: 500px;
    position: relative;
    // background-color: red;
    background-image: url('https://avada.theme-fusion.com/marketing-consultant/wp-content/uploads/sites/142/2020/06/marketing-intro.jpg');
    background-position: center;
    background-size: cover;
    .jumbo-demo{
        width: 60px;
        height: 60px;
        background-color: white;
        border-radius: 5px;
        text-align: center;
        position: absolute;
        right: 10px;
        top: 10px;
    }
    .jumbo-price{
        width: 60px;
        height: 60px;
        background-color: white;
        border-radius: 5px;
        text-align: center;
        position: absolute;
        right: 10px;
        top: 80px;
        padding: 5px 0;
        .price-text{
            display: flex;
            margin-left: 5px;

            p{
                font-size: 21px;
                color: #F85D00;
            }
        }
    }
    .jumbo-text {
        width: 50%;
        margin-top: 70px;
        color:  white;
        p {
            font-size: 18px;
            margin: 20px 0;
        }
        .jumbo-btn{
            border: none;
            padding: 8px 25px;
            border-radius: 7px;
        }
    }
    .jumbo-right{
        width: 50%;
        height: 100%;
        margin-top: 70px;
    
    }
}

.jumbo-form{
    width: 350px;
    height: 450px;
    border-radius: 8px;
    box-shadow: 0 10px 20px black;
    background-color: white;
}
</style>