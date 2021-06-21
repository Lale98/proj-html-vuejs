<template>
    <div id="main">
        <section id="consultation">
            <div class="ms_container interest">
                <div class="image">
                    <img src="" alt="img"> 
                </div>
                <div class="text">
                    <h4>Business Growth</h4>
                    <h2>Increase Brand Awareness</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente repellat expedita enim perspiciatis esse provident, a suscipit id, porro rerum, maxime ducimus nesciunt? Quia, dicta!</p>
                    <button class="btn btnOrange">Get a Consultation</button>
                </div>
            </div>
            <div class="ms_container interest">
                <div class="text">
                    <h4>Investitors In People</h4>
                    <h2>In-House Sales Training</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente repellat expedita enim perspiciatis esse provident, a suscipit id, porro rerum, maxime ducimus nesciunt? Quia, dicta!</p>
                    <button class="btn btnOrange">Get a Consultation</button>
                </div>
                <div class="image">
                    <img src="" alt="im"> 
                </div>
            </div>
            <div class="ms_container interest">
                <div class="image">
                    <img src="" alt="img"> 
                </div>
                <div class="text">
                    <h4>Social Media Analysis</h4>
                    <h2>Harness Your Social Proof</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente repellat expedita enim perspiciatis esse provident, a suscipit id, porro rerum, maxime ducimus nesciunt? Quia, dicta!</p>
                    <button class="btn btnOrange">Get a Consultation</button>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
export default {
    name : "Main",
}
</script>

<style lang="scss" scoped>
    .interest {
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        
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