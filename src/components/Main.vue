<template>
    <div id="main">
        <section id="consultation">
            <div class="ms_container interest">
                <div class="image">
                    <img src="../assets/images/img1.svg" alt="img"> 
                </div>
                <div class="text">
                    <div class="align-center">
                        <div class="ball blue"></div>
                        <h4>Business Growth</h4>
                    </div>
                    <h2>Increase Brand Awareness</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente repellat expedita enim perspiciatis esse provident, a suscipit id, porro rerum, maxime ducimus nesciunt? Quia, dicta!</p>
                    <button class="btn btnOrange">Get a Consultation</button>
                </div>
            </div>
            <div class="ms_container interest">
                <div class="text">
                    <div class="align-center">
                        <div class="ball yellow"></div>
                        <h4>Investitors In People</h4>
                    </div>
                    <h2>In-House Sales Training</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente repellat expedita enim perspiciatis esse provident, a suscipit id, porro rerum, maxime ducimus nesciunt? Quia, dicta!</p>
                    <button class="btn btnOrange">Get a Consultation</button>
                </div>
                <div class="image">
                    <img src="../assets/images/img2.svg" alt="im"> 
                </div>
            </div>
            <div class="ms_container interest">
                <div class="image">
                    <img src="../assets/images/img3.svg" alt="img"> 
                </div>
                <div class="text">
                    <div class="align-center">
                        <div class="ball green"></div>
                        <h4>Social Media Analysis</h4>
                    </div>
                    <h2>Harness Your Social Proof</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente repellat expedita enim perspiciatis esse provident, a suscipit id, porro rerum, maxime ducimus nesciunt? Quia, dicta!</p>
                    <button class="btn btnOrange">Get a Consultation</button>
                </div>
            </div>
        </section>
        <section id="brands">
            <h2>Some Brands We Work With</h2>
            <p>Quisque aliquet, libero consequat elementum convallis.</p>
            <div class="brand align-center space-bet ms_container ">
                <img v-for="brand,index in brands" :key="index" :src="require(`../assets/images/${brand.img}`)" alt="brand">
            </div>
        </section>
        <div class="contact ms_container align-center space-bet">
            <div class="align-center">
                <img src="../assets/images/marketing-expert-cta.png" alt="profilo">
                <div class="nameInfo">
                    <h4>Sandy Reiff</h4>
                    <p>Marketing Consultant Expert</p>
                </div>
                <h3>Drive Leads and Sales with Avada</h3>
            </div>
            <button class="btn btnLightOrange">
                <div class="phone">
                    <i class="fas fa-phone-alt orange"></i>
                    <p class="orange">{{phone}}</p>
                </div>
            </button>
        </div>
        <h2 class="txt-center">Trusted by Leading Organisations</h2>
        <section class="ms_container">
            <Card :persons="persons" id="persons"/>
            <div class="person txt-center">
                <button class="btn btnOrange">Read More Case Studies</button>
            </div>
        </section>
        <section id="work">
            <div class="ms_container space-bet work-us">
                <div class="txt">
                    <h2>We Boost Our Clients’ Bottom Line by Optimizing Their Growth Potential.</h2>
                    <p>Quisque aliquet, libero consequat elementum convallis, erat risus imperdiet pellentesque sem neque eget.</p>
                    <button class="btn btnOrange">Why Work With Us</button>
                </div>
                <img src="../assets/images/we-boost-our-clients.jpg" alt="boost">
            </div>
            <div class="ms_container space-bet">
                <div class="txt-1">
                    <h2>We Build Relationships</h2>
                    <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur.</p>
                    <h2>Proprietary Processes</h2>
                    <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur.</p>
                </div>
                <div class="list">
                    <div class="item">
                        <div class="square"></div>
                        <div class="txt-info">
                            <h3>Accountability</h3>
                            <p>Curabitur ac leo nunc vestibulum</p>
                        </div>
                    </div>
                    <div class="item">
                        <div class="square"></div>
                        <div class="txt-info">
                            <h3>Transparency</h3>
                            <p>Curabitur ac leo nunc vestibulum</p>
                        </div>
                    </div>
                    <div class="item">
                        <div class="square"></div>
                        <div class="txt-info">
                            <h3>Investment</h3>
                            <p>Curabitur ac leo nunc vestibulum</p>
                        </div>
                    </div>
                </div>
            </div>
            <h3 class="txt-center awards-title">Awards</h3>
            <section id="awards" class="ms_container space-bet">
                <div v-for="award,index in awards" :key="index" class="txt-center">
                    <img :class="award.color" :src="require(`../assets/images/award-${award.img}`)" alt="award">
                    <p>{{award.title}}</p>
                    <p>{{award.info}}</p>
                </div>
            </section>
            <div class="testimonial ms_container space-evenly">
                <img src="../assets/images/large-testimonial.jpg" alt="testimonial">
                <div class="txt w30">
                    <h3>“The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online and offline. We have experienced year on year growth due to their progressive approach.”</h3>
                    <h4>Kate Schadler</h4>
                    <h6>Marketing Consultant - Abstract</h6>
                </div>
            </div>
            <div id="resouces">
                
            </div>
        </section>
    </div>
</template>

<script>
import Card from './Card.vue';

export default {
    name : "Main",
    props : {
        brands : Array,
        phone : String,
        awards : Array,


    },
    components: {
        Card,
    },
    data : function () {
        return {
            persons : [
                {
                img : '1',
                txt : 'How Spaces attracted five million visitors by improving the content',
                num : '200%',
                info : 'Higher revenue from digital'
                },
                {
                img : '4',
                txt : 'Creativity helped \n Hemisferio to increase their brand reach vertically',
                num : '10x',
                info : 'Sales increase with the same ad spend'
                },
                {
                img : '6',
                txt : 'How DigitalBox used Al-powered data insight to boost sales',
                num : '3-year',
                info : 'Partnership with Avada Consultant'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/variables';
    .testimonial {
        .w30 {
            margin-top: 50px;
            width: 30%;
        }
        img {
            width: 47%;
            border-radius: 15px;
            margin-right: 50px;
        }
    }
    #awards {
        margin-bottom: 200px;
        img {
            width: 60%;
        }
        p {
            font-size: 20px;
            margin-bottom: 10px;
        }
    }
    .awards-title {
        margin: 60px 0;
    }
    .red {
        filter: saturate(400%);
        opacity: 0.7;
    }
    .light-blue {
        filter: sepia(100%) hue-rotate(170deg) saturate(500%) brightness(100%);
    }
    .blu {
        filter: sepia(100%) hue-rotate(195deg) saturate(500%) brightness(90%);
    }
    .list {
        width: 45%;
    }
    .item {
        display: flex;
        margin-bottom: 70px;
    }
    .square {
        border: 2px solid $colorOrange;
        border-radius: 15px;
        height: 75px;
        width: 75px;
        margin-right: 30px;
    }
    .txt-info {
        h3 {
            font-size: 25px;
            font-weight: 450;
            margin-bottom: 20px;
        }
        p {
            font-size: 20px;
        }
    }
    .txt-1 {
        width: 40%;
        h2 {
            font-size: 35px;
            font-weight: 450;
            margin: 0;

            &:last-of-type {
                margin-top: 100px;
            }
        }
        p {
            font-size: 20px;
            line-height: 30px;
            margin: 20px 0;
        }
    }
    .txt {
        padding-top: 50px;
        width: 35%;
        h2 {
            font-size: 50px;
            margin: 0;
        }
        h4 {
            font-weight: 450;
            font-size: 20px;
        }
        h3 {
            font-weight: 450;
            font-size: 30px;
            line-height: 42px;
            margin-bottom: 20px;
        }
        h6 {
            font-weight: 400;
            font-size: 14px;
            margin-top: 10px;
        }
        p {
            font-size: 22px;
            line-height: 35px;
            margin: 20px 0;
        }
    }
    #work {
        padding: 150px;
        background-color: rgba(#E3E4E2,0.3);
    }
    #work .work-us img {
        width: 50%;
        border-radius: 15px;
        margin-bottom: 150px;
    }
    #persons {
        margin-bottom: 100px;
    }
    .person button {
        margin-bottom: 150px;
    }
    h2 {
        font-size: 50px;
        margin: 70px;
    }
    .nameInfo {
        margin-left: 15px;
        margin-right: 80px;
        h4 {
            font-size: 22px;
            font-weight: 450;
        }
        p {
            font-size: 15px;
        }
    }
    .contact {
        margin: 150px auto;
        border-radius: 15px;
        padding: 15px 30px;
        box-shadow: 0 15px 40px rgba(black, 0.2);

        h3 {
            font-size: 24px;
            font-weight: 450;
        }
        img {
            border-radius: 50%;
            width: 70px;
        }
    }
    #brands {
        text-align: center;
        
        h2 {
            font-size: 50px;
            margin-bottom: 30px;
        }
        p {
            font-size: 22px;
            margin-bottom: 60px;
        }
        img {
            height: 50px;
        }
    }
    .interest {
        height: 80vh;
        display: flex;
        align-items: center;
        justify-content: space-between;

        img {
            height: 600px;
        }
        
        .text {
            width: 40%;
            padding: 40px;

            h2 {
                font-size: 50px;
                line-height: 55px;
                margin: 25px 0;
            }
            h4 {
                font-size: 22px;
                font-weight: 400;
            }
            p {
                font-size: 24px;
                line-height: 35px;
            }
            button {
                margin-top: 25px;
            }
        }
    }
</style>