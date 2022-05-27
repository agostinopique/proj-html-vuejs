<template>
    <div class="header-container">
        <div class="container d-flex justify-content-between align-items-center">
            <div class="header-logo">
                <img src="../assets/img/avada-marketing-logo.png" alt="avada-logo">
            </div>
            <div class="header-nav">
                <nav>
                    <ul>
                        <li>MENU</li>
                        <li>MENU</li>
                        <li>MENU</li>
                        <li>MENU</li>
                        <li>MENU</li>
                        <li>MENU</li>
                    </ul>
                </nav>
            </div>
            <div class="contacts">
                <div class="d-flex align-items-center">
                    <i class="bi bi-telephone-fill"></i>
                    <p>(555) 802-1234</p>
                    <button class="btn header-btn">Free Quote</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    naame: 'HeaderComp'
}
</script>

<style lang="scss" scoped>
.header-container {
    width: 100%;
    height: 90px;
    background-color: white;

    border: 1px solid black;

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
            margin-left: 10px;
        }

        i{
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
            margin: 0 10px;
        }
    }
}
</style>