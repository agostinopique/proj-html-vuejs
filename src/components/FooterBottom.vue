<template>
    <div class="footer-container">
        <div class="footer-lists">

            <div class="footer-info">
                <h2>Grow Your online Business Strategically and Improve Customer Retention</h2>
                <ul class="social-icons">
                    <li><i class="fa-brands fa-facebook-f fa-2x"></i></li>
                    <li><i class="fa-brands fa-twitter fa-2x"></i></li>
                    <li><i class="fa-brands fa-instagram fa-2x"></i></li>
                    <li><i class="fa-brands fa-youtube fa-2x"></i></li>
                    <li><i class="fa-brands fa-linkedin-in fa-2x"></i></li>
                    <li><i class="fa-brands fa-tiktok fa-2x"></i></li>
                </ul>
            </div>
            <FooterListComp 
                v-for="(list, index) in listData"
                :key="`list item-${index}`"
                :listItem="list"/>
        </div>
        <div class="bottom-links">
            <p><i class="fa-regular fa-copyright"></i> • Avada Consultant • Powered by WordPress</p>
            <p>Call Us (555) 802-1234</p>
            <p><a href="#">info@yourcompany.com</a></p>
        </div>
    </div>
</template>

<script>
import FooterListComp from './FooterListComp.vue';

import footerListData from '../assets/script/footerListData';

export default {
    name: "FooterBottom",
    components: { FooterListComp },
    data(){
        return {
            listData: footerListData
        }
    }
}
</script>

<style lang="scss" scoped>
@import '~@fortawesome/fontawesome-free/css/all.min.css';

.footer-container {
    width: 80%;
    margin: 0 auto;
    height: 50vh;
    padding: 60px 0;
    .footer-lists{
        display: flex;
        justify-content: space-between;
        margin-bottom: 40px;
    }
    .footer-info{
        width: 30%;
        h2{
            font-size: 3rem;
        }
        .social-icons{
            display: flex;
            justify-content: flex-start;
            align-items: center;
            list-style: none;
            padding-left: 0;
            li{
                margin: 20px 30px 0 0;
            }
        }
    }
    .bottom-links{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 100px;
    }
}
</style>