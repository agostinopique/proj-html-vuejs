<template>
    <div>
        <div class="footer-background">
            <FooterTop />
        </div>
        <FooterBottom />
    </div>
</template>

<script>
import FooterTop from './FooterTop.vue';
import FooterBottom from './FooterBottom.vue';

export default {
    name: 'FooterComp',
    components: {
        FooterTop,
        FooterBottom
    }
}
</script>

<style lang="scss" scoped>
.footer-background{
    background-color: black;
}
</style>