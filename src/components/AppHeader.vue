<script>
import HeaderNav from './HeaderNav.vue';

export default {
    name: "AppHeader",
    data() {
        return {
            words:['Ready', 'Professional','Expert'],
            index:0,
        };
    },

    components: { HeaderNav },

    methods:{
        // funzione che cambia l'index per il carosello : lo aumenta fino a quando non raggiungela lunghezza dell'array words e poi lo riazzera
        changeTitle(){
            this.index++

            if(this.index == this.words.length){
                this.index = 0
            }
        }
    },
    // al caricamento della pagina si avvia un setIntervall che richiama la funzione che mi fa aumentare l'indice a intervalli di 5 secondi
    mounted() {
        setInterval(this.changeTitle, 5000)
    },

}
</script>

<template>
    <div class="container">

        <HeaderNav></HeaderNav>

        <div class="text-box">
            <h1>{{ words[index] }} <mark>Team</mark> </h1>

            <p>No matter what your company needs, we will be <br> ready to assist you in the best possible way</p>

            <div class="btn-container">
                <button class="btn1">Get in touch</button>
                <button class="btn2">Read More</button>

            </div>

            <div class="carusell">
                <div class="active first" :style="index == 0 ? {backgroundColor:'#058283'} : {backgroundColor: 'white'}">

                </div>

                <div class="active second" :style="index == 1 ? {backgroundColor:'#058283'} : {backgroundColor: 'white'}">

                </div>

                <div class="active third" :style="index == 2 ? {backgroundColor:'#058283'} : {backgroundColor: 'white'}">
                    
                </div>
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
        position: relative;
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

        .carusell{

            .active{
                border: 1px solid grey;
                border-radius: 10px;
                width: 6px;
                height: 20px;
                right: 20px;
                position: absolute;
            }

            .first{
                top: 30%;
            }
            .second{
                top: 45%;
            }

            .third{
                top: 60%;
            }
        }

        
    }
}
    
</style>