<script>
import HeaderNav from './HeaderNav.vue';

export default {
    name: "AppHeader",
    data() {
        return {};
    },
    components: { HeaderNav }
}
</script>

<template>
    <div class="container">

        <HeaderNav></HeaderNav>

        <div class="text-box">
            <h1>Ready <mark>Team</mark> </h1>

            <p>No matter what your company needs, we will be <br> ready to assist you in the best possible way</p>

            <div class="btn-container">
                <button class="btn1">Get in touch</button>
                <button class="btn2">Read More</button>
            </div>

        </div>

    </div>
    
</template>

<style lang="scss" scoped>
.container{
    min-height: 600px;
    background-image: url('img/bg-parallax.png') ;
    background-position: center;
    background-size: 2700px;

    .text-box{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
    
        margin-top: 150px;

        p{
            text-align: center;
        }

        .btn-container{
            display: flex;
            gap: 10px;
        }
    }
}
    
</style>