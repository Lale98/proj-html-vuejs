<template>
    <div class="space-bet">
        <div v-for="person,index in persons" :key="index" class="card">
            <img :src="require(`../assets/images/case-studies-${person.img}.jpg`)" alt="person">
            <h3>{{person.txt}}</h3>
            <h2>{{person.num}}</h2>
            <p>{{person.info}}</p>
            <div class="back"></div>
        </div>
    </div>
</template>

<script>
export default {
    name : "Card",
    props : {
        persons : Array,

    }

}
</script>

<style lang="scss" scoped>
@import '../assets/variables';
    .back {
        height: 450px;
    }
    .card {
        position: relative;
        width: calc((100% - 100px) / 3);

        h3 {
            font-size: 32px;
            font-weight: 450;
            margin-top: 20px;
            margin-bottom: 40px;
        }
        h2 {
            font-size: 50px;
            margin-bottom: 5px;
        }
        p {
            font-size: 20px;
        }
        img {
            width: 100%;
        }
    }
</style>