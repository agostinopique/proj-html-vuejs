<template>
    <div class="header-container">
        <div class="container d-flex justify-content-between align-items-center">
            <div class="header-logo">
                <img src="../assets/img/avada-marketing-logo.png" alt="avada-logo">
            </div>
            <div class="header-nav">
                <nav>
                    <ul>
                        <li v-for="(comp, index) in headerElements"
                            :key="index"
                            :class="comp.isActive ? 'active' : ''">{{comp.name}}
                            <i v-if="comp.chevron === true" class="bi bi-chevron-down"></i>
                        </li>
                    </ul>
                </nav>
            </div>
            <div class="contacts">
                <div class="d-flex align-items-center">
                    <i class="bi bi-telephone-fill phone"></i>
                    <p>(555) 802-1234</p>
                    <button class="header-btn">Free Quote</button>
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
.header-container {
    width: 100%;
    height: 90px;
    background-color: white;
    .container{ 
        height: 100%;
    }
    .header-nav,
    .contacts {
        display: flex;
        align-items: center;
        height: 100%;

        .header-btn{
            background-color: #FFE7DA;
            color: #F85D00;
            margin-left: 30px;
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
        display: flex;
        align-items: center;
        list-style: none;
        margin-bottom: 0;

        li{
            padding: 0 5px;
            margin: 5px 20px;
            &.active{
                border-bottom: 2px solid #F85D00;
                color: #F85D00;
            }
        }
    }
}
</style>