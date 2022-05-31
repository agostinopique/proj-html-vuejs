<template>
    <div class="footer-container">
        <div class="footer-left">
            <h2>Let's Make Things Happen</h2>
            <p class="footer-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos sed pariatur natus voluptas ratione ipsam reiciendis quod explicabo.</p>
            <div class="divider-hr"></div>
            <p class="testimonial-text">"The team at Avada Marketing Consultant is fabulous. They helped ut unlock our potential oline and offline. We have axperienced year on year growth due to their progressive approach"</p>
            <span class="testimonial-name">George Anderson</span>
            <span class="testimonial-role">DigitalBox CEO</span>
        </div>
        <div class="footer-right">
            <div class="footer-form">

                <div class="profile-info">
                    <img src="../assets/img/marketing-consultant-expert.jpg" alt="consultant-expert">
                    <h4>Richard Madsen</h4>
                    <p class="role">Marketing Consultant Expert</p>
                    <p class="phone"><i class="bi bi-telephone-fill phone"></i> (555) 802-1234</p>
                </div>
                <div class="footer-inputs">
                    <input type="text" placeholder="Your Name*">
                    <img class="input-img" src="../assets/img/image.png" alt="">
                    <input type="email" placeholder="Your Email*">
                    <input type="phone" placeholder="Your Phone Number*">
                    <button id="hover-btn" class="footer-btn">Get a Callback</button>
                    <p class="footer-terms">By submitting my data I agree to be contacted</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterTop'
}
</script>

<style lang="scss" scoped>
.footer-container{
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 70%;
    margin: 0 auto;
    padding: 80px 0;
    .footer-right,
    .footer-left{
        width: 50%;
    }
}
.footer-right{
    display: flex;
    flex-direction: column;
    align-items: center;
}
.footer-left{
    color: white;
    h2{
        font-size: 60px;
    }
    .footer-text{
        font-size: 22px;
        margin: 30px 30px 30px 0;
    }
    .divider-hr{
        width: 10%;
        height: 2px;
        background-color: grey;
        margin-bottom: 30px;
    }
    .testimonial-text{
        margin-right: 30px;
        font-size: 25px;
    }
    .testimonial-name{
        display: block;
        margin-top: 40px;
        font-size: 20px;
    }
    .testimonial-role{
        font-size: 18px;
        color: rgb(177, 174, 174);
    }
}
.footer-form{
    width: 350px;
    padding: 15px;
    text-align: center;
    border-radius: 8px;
    box-shadow: 0 10px 20px black;
    background-color: white;
    scale: 1.2;
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
    .footer-inputs{
        position: relative;
        input {
            width: 100%;
            padding: 10px 10px;
            border-radius: 5px;
            border-style: solid;
            margin: 6px 0;
        }
        .footer-btn{
            border: none;
            width: 100%;
            padding: 8px 0;
            border-radius: 7px;
            background-color: #F86011;
            color: white;
            margin-top: 15px;
        }
        .footer-terms {
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