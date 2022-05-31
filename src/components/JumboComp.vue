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
        <div class="ap-container">
            <div class="jumbo-text">
                <h1>Unlock Your Online <br> Growth Potential</h1>
                <p>Online marketing to secure customer retention, <br> leads, and sales. We focus on the bigger picture.</p>
                <button id="transparent-hover" class="jumbo-btn">Our Services <i class="bi bi-arrow-right-short"></i></button>
            </div>
            <div class="jumbo-right">
                <div class="jumbo-form">

                    <div class="profile-info">
                        <img src="../assets/img/marketing-consultant-expert.jpg" alt="consultant-expert">
                        <h4>Richard Madsen</h4>
                        <p class="role">Marketing Consultant Expert</p>
                        <p class="phone"><i class="bi bi-telephone-fill phone"></i> (555) 802-1234</p>
                    </div>
                    <div class="jumbo-inputs">
                        <input type="text" placeholder="Your Name*">
                        <img class="input-img" src="../assets/img/image.png" alt="">
                        <input type="email" placeholder="Your Email*">
                        <input type="phone" placeholder="Your Phone Number*">
                        <button id="hover-btn" class="jumbo-btn">Get a Callback</button>
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
@import '../assets/style/mixins';

.jumbotron {
    height: 690px;
    @include dFlexAlignCenter; 
    position: relative;
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
    .ap-container{
        @include dFlexBetween;
        width: 70%;
        margin: 0 auto;
    }
    .jumbo-text {
        margin-top: 60px;
        color:  white;
        h1{
            font-size: 4rem;
            font-weight: bold;
            text-transform: capitalize;
        }
        p {
            font-size: 30px;
            margin: 20px 0;
        }
        .jumbo-btn{
            border: none;
            padding: 12px 30px;
            border-radius: 7px;
            font-size: 20px;
        }
    }
    .jumbo-right{
        position: relative;
        width: 40%;
        top: 70px;
    }
}

.jumbo-form{
    width: 480px;
    height: 600px;
    padding: 15px;
    text-align: center;
    border-radius: 8px;
    box-shadow: 0 10px 20px rgb(178, 177, 177);
    background-color: white;
    font-size: 1.5rem;
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
        .role{
            font-size: 15px;
            color: rgb(157, 154, 154);
        }
        .phone {
            margin-top: 15px;
            color: #F86011;
        }
    }
    .jumbo-inputs{
        position: relative;
        input {
            width: 95%;
            padding: 10px 10px;
            border-radius: 8px;
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
            top: 30px;
            right: 20px;
        }
    }
}
</style>