@include dFlexBetween;<template>
    <div class="footer-container">
        <div class="footer-lists">

            <div class="footer-info">
                <h2>Grow Your online Business Strategically and Improve Customer Retention</h2>
                <ul class="social-icons">
                    <li><i class="fa-brands fa-facebook-f"></i></li>
                    <li><i class="fa-brands fa-twitter"></i></li>
                    <li><i class="fa-brands fa-instagram"></i></li>
                    <li><i class="fa-brands fa-youtube"></i></li>
                    <li><i class="fa-brands fa-linkedin-in"></i></li>
                    <li><i class="fa-brands fa-tiktok"></i></li>
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
@import '../assets/style/mixins';

.footer-container {
    width: 80%;
    margin: 0 auto;
    height: 50vh;
    padding: 60px 0;
    .footer-lists{
        @include dFlexBetween;
        margin-bottom: 40px;
    }
    .footer-info{
        width: 30%;
        h2{
            font-size: 2rem;
        }
        .social-icons{
            @include dFlexAlignCenter;
            justify-content: flex-start;
            list-style: none;
            padding-left: 0;
            li{
                margin: 20px 30px 0 0;
                i{
                    font-size: 25px;
                }
            }
        }
    }
    .bottom-links{
        @include dFlexAlignCenterBetween;
        margin-top: 100px;
    }
}
</style>