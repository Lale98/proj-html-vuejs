<template>
    <div id="header">
        <div id="nav_bar">
            <div class="ms_container">
                <div class="nav_left">
                    <img id="logo" src="../assets/images/avada-marketing-logo.png" alt="logo">
                    <ul>
                        <li v-for="data, index in navBarData" :key="index">
                            <a href="">{{data.name}}</a>
                            <i v-if="data.list == true" class="fas fa-chevron-down"></i>
                        </li>
                    </ul>
                </div>
                <div class="nav_right">
                    <div class="phone">
                        <i class="fas fa-phone-alt orange"></i>
                        <p>(555) 802-1234</p>
                    </div>
                    <button class="btn orange backLightOrange">Free Quote</button>
                </div>
            </div>
        </div>
        <div id="jumbotron">
            
        </div>
    </div>
</template>

<script>
export default {
    name : "Header",
    props : {
        navBarData : Array,
    }
}
</script>

<style lang="scss" scoped>
@import '~@fortawesome/fontawesome-free/css/all.min.css';

    #nav_bar {
        height: 10vh;

        .ms_container {
            margin: 0 auto;
            max-width: 1300px;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .nav_left {
            display: flex;
            justify-content: flex-start;
        }

        .nav_right {
            display: flex;
            justify-content: flex-end;

            .phone {
                margin-right: 20px;
            }
        }
    }
    .phone {
        display: flex;
        align-items: center;
        i {
            margin-right: 20px;
        }
    }
    ul {
        list-style: none;
        display: flex;


        li {
            font-size: 18px;
            font-weight: 500;
            display: flex;
            align-items: center;

            a {
                text-decoration: none;
                color: black;
                margin-left: 30px;
                padding-right: 5px;
            }
        }
    }

</style>