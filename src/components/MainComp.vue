<template>
<div>
    <JumboComp />
    <CardComp
        v-for="(card, index) in cardElements"
        :key="`Card-${index}`"
        :cardElement="card"
        :cardIndex="index" />
    <PartBrandComp />

    <div class="expert-profile">
        <div class="expert-info">
            <div class="expert-img">
                <img src="../assets/img/marketing-expert-cta.png" alt="marketing-expert">
            </div>
            <div class="expert-name">
                <p>Sandy Reiff</p>
                <span>Marketing Consultant Expert</span>
            </div>
        </div>
        <div class="expert-role">
            <p>Drive Leads and Sales with Avada</p>
        </div>
        <div class="expert-number">
            <button id="light-hover" class="expert-btn"><i class="bi bi-telephone-fill phone"></i>(555) 802-1234</button>
        </div>
    </div>

    <MainBrandComp />
    <div class="secondary-card">
        <MiddleCardComp />
        <div class="core-values">
            <div class="core-left">
                <div class="core-top">
                    <h4>We Build Relationships</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing <br> elit. Ratione qui ipsam incidunt.</p>
                </div>
                <div class="core-bottom">
                    <h4>Proprietary Process</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing <br> elit. Ratione qui ipsam incidunt.</p>
                </div>
            </div>
            <div class="core-right">
                <div class="core-container">
                    <div class="core-icon"><i class="bi bi-file-earmark-text-fill"></i></div>
                    <div>
                        <p>Accountability</p>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
                
                <div class="core-container">
                    <div class="core-icon"><i class="bi bi-file-earmark-diff-fill"></i></div>
                    <div>
                        <p>Transparency</p>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
                
                <div class="core-container">
                    <div class="core-icon"><i class="bi bi-file-earmark-bar-graph-fill"></i></div>
                    <div>
                        <p>Investment</p>
                        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="award-section">
            <h3>Awards</h3>
            <div class="award-container">
                <AwardComp 
                    v-for="(award, index) in awardElements"
                    :key="index"
                    :award="award"/>
            </div>
        </div>
        <div class="avada-team">
            <div class="avada-img">
                <img src="../assets/img/large-testimonial-600x583.jpg" alt="avada-consultant">
            </div>
            <div class="avada-text">
                <p>"The team at Avada Marketing Consultant is fabulous. They helped ut unlock our potential oline and offline. We have axperienced year on year growth due to their progressive approach"</p>
                <span class="testimonial-name">Kate Schandler</span>
                <span class="testimonial-role">Marketing Consultant - Abstract</span>
            </div>
        </div>
    </div>
    <div class="bottom-main">
        <div class="ap-container">
            <div class="marketing-resources">
                <p>Marketing Resources: Insider Advice on How to Increase Online Sales</p>
                <button id="hover-btn" class="bottom-btn">Explore All Resources</button>
            </div>
            <div class="marketing-articles">
                <MarketingCards 
                    v-for="(tip, index) in marketingTips"
                    :key="`Tip-${index}`"
                    :tip="tip"/>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import JumboComp from './JumboComp.vue';
import CardComp from './CardComp.vue';
import PartBrandComp from './PartBrandComp.vue';
import MainBrandComp from './MainBrandComp.vue';
import MiddleCardComp from './MiddleCardComp';
import AwardComp from './AwardComp.vue';
import MarketingCards from './MarketingCardsComp.vue'

import cardElements from '@/assets/script/cardElements';
import awardElements from '../assets/script/awardElements';
import marketingTips from '../assets/script/marketingTips';


export default {
    name: 'MainComp',
    components: {
    CardComp,
    JumboComp,
    PartBrandComp,
    MainBrandComp,
    MiddleCardComp,
    AwardComp,
    MarketingCards
},
    data(){
        return{
            cardElements: cardElements,
            awardElements: awardElements,
            marketingTips: marketingTips
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';
.expert-profile{
    width: 70%;
    margin: 250px auto;
    @include dFlexAlignCenterBetween;
    border-radius: 10px;
    box-shadow: -15px 15px 20px lightgrey;
    padding: 10px 25px;
    .expert-info{
        @include dFlexAlignCenter;
        .expert-name span{ 
            font-size: 15px;
            color: #6A6A6A;
        }
        .expert-name p{
            font-size: 22px;
        }
    }
    .expert-role p{ 
        font-size: 25px;
    }
    .expert-img{ 
        width: 65px;
        margin-right: 20px;
        img{
            width: 100%;
            border-radius: 50%;
        }
    }
    .expert-btn{
            background-color: #FFE7DA;
            color: #F85D00;
            margin-left: 30px;
            padding: 10px 28px;
            border-radius: 7px;
            border-color: #FFE7DA;
            border-style: solid;
            font-size: 18px;
            i{
                margin-right: 10px;
            }
        }
}
.secondary-card{
    width: 100%;
    background: rgb(244,244,246);
    background: linear-gradient(180deg, rgba(244,244,246,1) 50%, rgba(255,255,255,1) 100%);
    margin-top: 80px;
    padding: 80px 0;
    .core-values{
        display: flex;
        width: 70%;
        margin: 0 auto;
    }
}
.core-left{
    width: 50%;
    margin-right: 60px;
    display: flex;
    justify-content: space-evenly;
    flex-direction: column;
    h4{
        margin-bottom: 20px;
    }
}
.core-right{
    width: 50%;
    @include dFlexBetween;
    flex-direction: column;
    .core-container {
        display: flex;
        align-items: center;
        margin: 20px 0;
    }
    .core-icon{
        width: 80px;
        height: 80px;
        text-align: center;
        line-height: 80px;
        border: 1px solid #F86011;
        border-radius: 15px;
        margin-right: 15px;
        i {
            color: #F86011;
            font-size: 25px;
        }
    }
}

.award-section{
    width: 70%;
    margin: 0 auto;
    margin-top: 90px;
    text-align: center;
    .award-container{
        @include dFlexBetween;
    }
}
.avada-team {
    @include dFlexAlignCenterBetween;
    width: 70%;
    margin: 150px auto;
    .avada-img {
        width: 50%;
    }
    .avada-img img{
        width: 100%;
        border-radius: 5px;
        box-shadow: 5px 5px 20px lightgrey;
    }
    .avada-text {
        width: 50%;
        padding-left: 180px;
        p{
            font-size: 23px;
        }
        .testimonial-name{
            display: block;
            margin-top: 40px;
        }
        .testimonial-role{
            font-size: 13px;
            color: rgb(177, 174, 174);
        }
    }
}
.bottom-main{
    background: rgb(244,244,246);
    background: linear-gradient(180deg, rgba(244,244,246,1) 50%, rgba(255,255,255,1) 100%);
    margin-top: 80px;
    margin-bottom: 110px;
}
.ap-container{
    width: 80%;
    margin: 0 auto;
    
    padding-top: 100px;
    .marketing-resources{
        @include dFlexBetween;
        align-items: flex-end;
        p {
            width: 30%;
            font-size: 35px;
            font-weight: bold;
        }
        .bottom-btn{
            background-color: #F86011;
            color: white;
            margin-left: 30px;
            padding: 8px 25px;
            border-radius: 7px;
            height: fit-content;
        }
        
    }

}
.marketing-articles {
    margin-top: 60px;
    @include dFlexBetween;
    flex-wrap: wrap;
}
</style>