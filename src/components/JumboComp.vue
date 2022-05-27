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
        <div class="container d-flex h-100">
            <div class="jumbo-text">
                <h1>Unlock Your Online <br> Growth Potential</h1>
                <p>Online marketing to secure customer retention, <br> leads, and sales. We focus on the bigger picture.</p>
                <button class="jumbo-btn">Our Services <i class="bi bi-arrow-right-short"></i></button>
            </div>
            <div class="jumbo-right">
                <div class="jumbo-form">

                    <div class="profile-info">
                        <img src="../assets/img/marketing-consultant-expert.jpg" alt="consultant-expert">
                        <h4>Richard Madsen</h4>
                        <p>Marketing Consultant Expert</p>
                        <p class="phone"><i class="bi bi-telephone-fill phone"></i> (555) 802-1234</p>
                    </div>
                    <div class="jumbo-inputs">
                        <input type="text" placeholder="Your Name*">
                        <img class="input-img" src="../assets/img/image.png" alt="">
                        <input type="email" placeholder="Your Email*">
                        <input type="phone" placeholder="Your Phone Number*">
                        <button class="jumbo-btn">Get a Callback</button>
                        <p class="jumbo-terms">By submitting my data I agree to be contacted</p>
                    </div>
                </div>
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


.jumbotron {
    height: 500px;
    position: relative;
    // background-color: red;
    background-image: url('https://avada.theme-fusion.com/marketing-consultant/wp-content/uploads/sites/142/2020/06/marketing-intro.jpg');
    background-position: center;
    background-size: cover;
    margin-bottom: 100px;
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
        margin-top: 60px;
        color:  white;
        h1{
            font-size: 3rem;
            text-transform: capitalize;
        }
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
        margin-top: 60px;
    
    }
}

.jumbo-form{
    width: 350px;
    height: 95%;
    padding: 15px;
    text-align: center;
    border-radius: 8px;
    box-shadow: 0 10px 20px black;
    background-color: white;
    .profile-info img{
        width: 60px;
        height: 60px;
        border-radius: 50%;
        margin-bottom: 10px;
    }

    .profile-info{
        h4{
            margin-bottom: 15px 0;
        }
        .phone {
            margin-top: 15px;
            color: #F86011;
        }
    }
    .jumbo-inputs{
        position: relative;
        input {
            width: 100%;
            padding: 10px 10px;
            border-radius: 5px;
            border-style: solid;
            margin: 6px 0;
        }
        .jumbo-btn{
            border: none;
            width: 100%;
            padding: 8px 0;
            border-radius: 7px;
            background-color: #F86011;
            color: white;
            margin-top: 15px;
        }
        .jumbo-terms {
            font-size: 14px;
            color: #8d8f94;
            margin-top: 7px;
        }
        .input-img{
            position: absolute;
            top: 23px;
            right: 5px;
        }
    }
}
</style>