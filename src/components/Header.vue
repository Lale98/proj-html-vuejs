<template>
    <div id="header">
        <div id="nav_bar">
            <div class="ms_container space-bet align-center">
                <div class="nav_left">
                    <img id="logo" src="../assets/images/avada-marketing-logo.png" alt="logo">
                    <ul>
                        <li @click="change(index)" v-for="data, index in navBarData" :key="index" :class="{active : activeClass == index}" class="menu">
                            <a :class="{active : activeClass == index}">{{data.name}}</a>
                            <i v-if="data.list == true" class="fas fa-chevron-down"></i>
                            <div class="line" :class="{hidden : activeClass != index}"></div>
                        </li>
                    </ul>
                </div>
                <div class="nav_right">
                    <div class="phone">
                        <i class="fas fa-phone-alt orange"></i>
                        <p class="bold">{{phone}}</p>
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
                            <div class="orange bold">{{phone}}</div>
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
            <div class="demos square center align-center ">
                <i class="fas fa-folder-open"></i>
                <p>Demos</p>
            </div>
            <div class="on-sale square">
                <div class="cont center align-center">
                    <i class="fas fa-dollar-sign"></i>
                    <h6>39</h6>
                    <p>On Sale</p>
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
            activeClass : 0
        }
    },
    methods : {
        change : function (index) {
            this.activeClass = this.navBarData[index].num;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import '../assets/variables';

    #jumbotron {
        height: 72vh;
        background-image: url("../assets/images/marketing-intro.jpg");
        background-size: cover;
        background-position-x: -110px;
        margin-top: 10vh;

        .veil {
            height: 100%;
            background-color: rgba(black, 0.2);
            padding-top: 5%;
        }
        
    }
    .square {
        flex-direction: column;
        height: 65px;
        width: 65px;
        border-radius: 7px;
        background-color: white;
        box-shadow: 0 0 5px rgba(black, 0.5);
        cursor: pointer;

        
        p {
            font-size: 12px;
        }
    }
    .on-sale {
        position: fixed;
        top: 223px;
        right: 15px;

        .cont {
            height: 100%;
            width: 100%;
            position: relative;
            flex-direction: column;

            h6 {
                font-size: 26px;
                color: #69BE7E;
                margin-left: 15px;
            }

            i {
                color: #69BE7E;
                position: absolute;
                top: 20%;
                left: 18%;
            }
        }
    }
    .demos {
        position: fixed;
        top: 150px;
        right: 15px;
        i {
            font-size: 25px;
            margin-bottom: 8px;
        }
    }
    .line {
        position: absolute;
        border: 1px solid $colorOrange;
        width: 80px;
        top: 85%;
        left: 25%;
    }
    .hidden {
        display: none;
    }
    .menu {
        position: relative;

        i {
            font-size: 12px;
        }
        a {
            cursor: pointer;
        }
        
    }
    .active {
        color: $colorOrange;
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
        position: fixed;
        height: 10vh;
        top: 0;
        width: 100%;
        background-color: white;
        z-index: 1;

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