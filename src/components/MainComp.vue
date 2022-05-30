<template>
<div>
    <JumboComp />
    <CardComp
        v-for="(card, index) in cardElements"
        :key="`Card-${index}`"
        :cardElement="card"
        :cardIndex="index" />
    <PartBrandComp />

    <div class="container expert-profile">
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
            <button class="expert-btn"><i class="bi bi-telephone-fill phone"></i>(555) 802-1234</button>
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
    </div>
</div>
</template>

<script>
import JumboComp from './JumboComp.vue';
import CardComp from './CardComp.vue';
import PartBrandComp from './PartBrandComp.vue';
import MainBrandComp from './MainBrandComp.vue';
import MiddleCardComp from './MiddleCardComp';
import AwardComp from '@/components/AwardComp';

import cardElements from '@/assets/script/cardElements';
import awardElements from '../assets/script/awardElements';

export default {
    name: 'MainComp',
    components: {
    CardComp,
    JumboComp,
    PartBrandComp,
    MainBrandComp,
    MiddleCardComp,
    AwardComp,
},
    data(){
        return{
            cardElements: cardElements,
            awardElements: awardElements
        }
    }
}
</script>

<style lang="scss" scoped>
.expert-profile{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 70px;
    margin-top: 50px;
    border-radius: 10px;
    box-shadow: -15px 15px 20px lightgrey;
    padding: 10px 25px;
    .expert-info{
        display: flex;
        align-items: center;
        .expert-name span{ 
            font-size: 14px;
            color: #6A6A6A;
        }
        .expert-name p{
            font-size: 20px;
        }
    }
    .expert-role p{ 
        font-size: 20px;
    }
    .expert-img{ 
        width: 50px;
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
            padding: 8px 25px;
            border-radius: 7px;
            border-color: #FFE7DA;
            border-style: solid;
            i{
                margin-right: 5px;
            }
        }
}
.secondary-card{
    width: 100%;
    background-color: #F6F6F7;
    margin-top: 80px;
    padding: 80px 0;
    .core-values{
        display: flex;
        align-content: center;
        width: 70%;
        margin: 0 auto;
        .core-top{
            margin: 40px 0;
        }
    }
}
.core-left{
    width: 50%;
    margin-right: 60px;
    h4{
        margin-bottom: 20px;
    }
}
.core-right{
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    .core-container {
        display: flex;
        align-items: center;
    }
    .core-icon{
        width: 60px;
        height: 60px;
        text-align: center;
        line-height: 60px;
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
        display: flex;
        justify-content: space-between;
    }
}
</style>