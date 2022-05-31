<template>
    <div class="header-container">
        <div class="ap-container d-flex justify-content-between align-items-center">
            <div class="header-logo">
                <img src="../assets/img/avada-marketing-logo.png" alt="avada-logo">
            </div>
            <div class="header-nav">
                <nav>
                    <ul>
                        <li v-for="(comp, index) in headerElements"
                            :key="index"
                            :class="comp.isActive ? 'active' : ''"><a href="#">{{comp.name}}</a>
                            <i v-if="comp.chevron === true" class="bi bi-chevron-down"></i>
                        </li>
                    </ul>
                </nav>
            </div>
            <div class="contacts">
                <div class="d-flex align-items-center">
                    <i class="bi bi-telephone-fill phone"></i>
                    <p>(555) 802-1234</p>
                    <button id="light-hover" class="header-btn">Free Quote</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import headerElements from '../assets/script/headerElements'


export default {
    name: 'HeaderComp',
    data(){
        return {
            headerElements: headerElements
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins';
.header-container {
    width: 70%;
    margin: 0 auto;
    height: 110px;
    background-color: white;
    .ap-container {
        height: 100%;
        @include dFlexBetween;
        align-items: center;
    }
    .header-nav,
    .contacts {
        @include dFlexAlignCenter;
        height: 100%;

        .header-btn{
            background-color: #FFE7DA;
            color: #F85D00;
            margin-left: 40px;
            padding: 8px 25px;
            border-radius: 7px;
            border-color: #FFE7DA;
            border-style: solid;
        }

        .phone {
            margin-right: 10px;
            color: #F85D00;
        }

        p{
            margin-bottom: 0;
        }
    }
    .header-nav nav ul{
        @include dFlexAlignCenter;
        list-style: none;
        margin-bottom: 0;

        li{
            margin: 10px 30px;
            font-size: 16px;
            a{
                text-decoration: none;
                color: black;
            }   
            &.active{
                border-bottom: 2px solid #F85D00;
                a{
                    color: #F85D00;
                }
            }
        }
    }
}
</style>