<template>
    <div id="header">
        <div id="nav_bar">
            <div class="ms_container space-bet align-center">
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
                        <p>{{phone}}</p>
                    </div>
                    <button class="btn orange btnLightOrange">Free Quote</button>
                </div>
            </div>
        </div>
        <div id="jumbotron">
            <div class="veil">
                <div class="ms_container space-bet">
                    <div class="j-left">
                        <h1>Unlock Your Online Growth Potential</h1>
                        <h3>Online marketing to secure custumers retention, leads, and sales. We focus on the bigger picture.</h3>
                        <button class="btn btnWhite">
                            Our Services
                            <i class="fas fa-arrow-right"></i>
                        </button>
                    </div>
                    <div class="callback">
                        <img :src="require(`../assets/images/${userInfo[callbackUserActive].img}`)" alt="profilo">
                        <h3>{{userInfo[callbackUserActive].name}}</h3>
                        <h4>{{userInfo[callbackUserActive].info}}</h4>
                        <div class="phone">
                            <i class="fas fa-phone-alt orange"></i>
                            <p class="orange">{{phone}}</p>
                        </div>
                        <form>
                            <input type="text" placeholder="Your Name*">
                            <img id="id" src="../assets/images/image.png" alt="image">
                            <input type="email" placeholder="Your Email*">
                            <input type="number" placeholder="Your Phone Number*">
                        </form>
                        <button class="btn-lg btnOrange">Get a Callback</button>
                        <p>By submitting my data I agree to be contacted</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : "Header",
    props : {
        navBarData : Array,
        phone : String,
        userInfo : Array,

    },
    data : function () {
        return {
            callbackUserActive : 0,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '~@fortawesome/fontawesome-free/css/all.min.css';
    #jumbotron {
        height: 72vh;
        background-image: url("../assets/images/marketing-intro.jpg");
        background-size: cover;
        background-position-x: -110px;

        .veil {
            height: 100%;
            background-color: rgba(black, 0.2);
            padding-top: 5%;
        }
        
    }
    .callback {
        background-color: white;
        width: 37%;
        height: 620px;
        margin-right: 7%;
        border-radius: 15px;
        box-shadow: 0 15px 40px rgba(black, 0.2);
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: space-around;
        padding: 20px 30px;

        img {
            border-radius: 50%;
            width: 80px;
        }

        h3 {
            font-size: 25px;
            font-weight: 420;
        }
        h4 {
            font-size: 20px;
            font-weight: 400;
            color: rgb(133, 135, 134);
        }

        input {
            position: relative;
            border: 1px solid rgba(133, 135, 134, 0.3);
            border-radius: 10px;
            width: 100%;
            padding: 15px 20px;
            font-size: 18px;
            margin-bottom: 15px;
        }
        p {
            font-size: 12px;
            color: rgb(133, 135, 134);
        }
    }
    form {
        position: relative;
    }
    #id {
        width: 18px;
        position: absolute;
        top: 9%;
        right: 4%;
    }
    .j-left {
        width: 50%;
        color: white;

        h1 {
            font-size: 70px;
            margin-bottom: 40px;
        }
        h3 {
            font-size: 28px;
            font-weight: 400;
            margin-bottom: 40px;
        }
        button {
            font-weight: 500;
            i {
                margin-left: 5px;
            }
        }
    }
    #nav_bar {
        height: 10vh;

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