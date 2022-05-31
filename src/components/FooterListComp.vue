<template>
    <div class="footer-list">
            <h5>{{listItem.title}}</h5>
            <ul>
                <li v-for="(li, index) in listItem.listElements"
                :key="index">
                    <a href="#">{{li}}</a>
                </li>
            </ul>
        </div>
</template>

<script>
export default {
    name: 'FooterListComp',
    props:{
        listItem: Object
    }
}
</script>

<style lang="scss" scoped>
.footer-list{
    width: 20%; 
    h5{
        margin-bottom: 15px;
    }
    ul{
        list-style: none;
        padding: 0;
        li{
            margin: 15px 0;
            font-size: 16px;
        }
        a{
            text-decoration: none;
            color: rgb(98, 94, 94);
        }
    }
}
</style>