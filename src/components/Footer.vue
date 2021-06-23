<template>
    <div id="footer">
        <div class="black-bg">
            <div class="ms_container space-bet">
                <div class="w40 white">
                    <h2>Let’s Make Things Happen</h2>
                    <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur.</p>
                    <hr>
                    <p class="p">“The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online and offline. We have experienced year on year growth due to their progressive approach.”</p>
                    <h4>George Anderson</h4>
                    <h5>Digitalbox CEO</h5>
                </div>
                <div class="callback">
                    <img :src="require(`../assets/images/${userInfo[callbackUserActive].img}`)" alt="profilo">
                    <h3>{{userInfo[callbackUserActive].name}}</h3>
                    <h4>{{userInfo[callbackUserActive].info}}</h4>
                    <div class="phone">
                        <i class="fas fa-phone-alt orange"></i>
                        <div class="orange">{{phone}}</div>
                    </div>
                    <form>
                        <input type="text" placeholder="Your Name*">
                        <input type="email" placeholder="Your Email*">
                        <input type="number" placeholder="Your Phone Number*">
                    </form>
                    <button class="btn-lg btnOrange">Get a Callback</button>
                    <p>By submitting my data I agree to be contacted</p>
                </div>
            </div>
        </div>
        <div id="call-us">
            <div class="ms_container space-bet">
                <div class="grow">
                    <h3>Grow Your Online Business Strategically, and Improve Customer Retention.</h3>
                    <ul class="inline-list">
                        <li>
                            <i class="fab fa-facebook-f"></i>
                        </li>
                        <li>
                            <i class="fab fa-twitter"></i>
                        </li>
                        <li>
                            <i class="fab fa-instagram"></i>
                        </li>
                        <li>
                            <i class="fab fa-youtube"></i>
                        </li>
                        <li>
                            <i class="fab fa-linkedin-in"></i>
                        </li>
                        <li>
                            <i class="fab fa-tiktok"></i>
                        </li>
                    </ul>
                </div>
                <div v-for="data,index in callUs" :key="index" class="links">
                    <h4>{{data.name}}</h4>
                    <ul>
                        <li v-for="link,index in data.links" :key="index">
                            {{link}}
                        </li>
                    </ul>
                </div>
            </div>
            <div class="ms_container space-bet contacts">
                <p>© 2020 • Avada Consultant • Powered by WordPress</p>
                <p>Call Us {{phone}}</p>
                <p>info@yourcompany.com</p>
            </div>
        </div>
        <div class="chat center align-center">
            <i class="fas fa-comment-alt"></i>
        </div>
    </div>
</template>

<script>
export default {
    name : "Footer",
    props : {
        userInfo : Array,
        callUs : Array,
        phone : String,
    },
    data : function () {
        return {
            callbackUserActive : 0,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/variables';
    .chat {
        position: fixed;
        bottom: 10px;
        right: 15px;
        background-color: $colorOrange;
        border-radius: 50%;
        height: 60px;
        width: 60px;
        cursor: pointer;

        i { 
            font-size: 25px;
            color: white;
        }

    }
    #call-us {
        padding: 100px 0;
        ul {
            list-style: none;

        }
        .inline-list {

            li {
                display: inline-block;
                font-size: 22px;
                margin-right: 20px;
                cursor: pointer;
            }
        }
    }
    .grow {
        width: 35%;

        h3 {
            font-size: 30px;
            font-weight: 450;
            margin-bottom: 40px;
        }
    }
    .contacts p:nth-child(2) {
        margin-right: 195px;
    }
    .links {
        margin-bottom: 100px;

        h4 {
            font-size: 20px;
            font-weight: 450;
        }
        li {
            font-size: 20px;
            font-weight: 400;
            margin: 15px 0;
            cursor: pointer;
        }
        &:last-child {
            margin-right: 100px;
        }
    }
    #footer {
        .black-bg {
            background-color: #010101;
            padding: 100px 0;
        }

        hr {
            border: 1px solid rgba(white,0.4);
            width: 100px;
            margin: 25px 0;
        }
        .white {
            color: white;

            .p {
                font-size: 25px;
                font-style: italic ;
            }
            p {
                font-size: 30px;
            }
            h2 {
                font-size: 65px;
                margin-bottom: 20px;
            }
            h4 {
                font-size: 20px;
                font-weight: 450;
                margin-top: 40px;
                margin-bottom: 15px;
            }
            h5 {
                font-weight: 400;
            }

        }

        .w40 {
            width: 45%;
        }
    }
</style>