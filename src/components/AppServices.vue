<script>
import ServicesCard from './ServicesCard.vue';

export default {
    name: "AppServices",
    data() {
        return {
            // array di oggetti con le proprietà di ogni card
            cards : [
                {
                    image: 'img/svg-1.svg',
                    title: 'Audit & Assurance',
                    description: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },

                {
                    image: 'img/svg-2.svg',
                    title: 'Financial Advisory',
                    description: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },

                {
                    image: 'img/svg-3.svg',
                    title: 'Analitycs and M&A',
                    description: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },

                {
                    image: 'img/svg-4.svg',
                    title: 'Middle Marketing',
                    description: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },

                {
                    image: 'img/svg-5.svg',
                    title: 'Legal Consulting',
                    description: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },

                {
                    image: 'img/svg-6.svg',
                    title: 'Regulatory Risk',
                    description: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },
            ]
        };
    },
    components: { ServicesCard }
}
</script>

<template>

    <div class="ext-container">

        <div class="services-box">
    
            <div class="left-box">
    
                <h5>Our Business Area</h5>
        
                <div class="title">
        
                    <h1>Exellence in <mark>Services</mark> </h1>
        
                </div>
        
                
                <p>
                    We are leaders in providing consultancy services with a set of cutting-edge tecnologies and a team of experienced and renowned professionals.
                    These are some options that you can hire.
                </p>
    
            </div>
    
            <div class="right-box">
                <button class="btn1">See All</button>
            </div>
        </div>

        <div class="services-card">
            <!-- creo tante card quanti sono gli elementi nell'array cards e passo le info a ServiceCard con le props -->
            <ServicesCard v-for="(card, index) in cards" :key="index" :img="card.image" :title="card.title" :info="card.description"></ServicesCard>

        </div>

    </div>
</template>

<style lang="scss" scoped >

.ext-container{

    background-color: #eef4ed;
     ;
}

.services-box{
    display: flex;
    

    max-width: 900px;
    margin: 0 auto;
    padding-top: 100px ;
    padding-bottom: 50px;

    .left-box{
        display: flex;
        flex-direction: column;
        gap: 20px;

        width: 80%;
        h5{
            text-transform: uppercase;
            color: #0dabb2;
        }
    
        .title{
            color: #333333;
            font-weight: 800;
        }
    
        p{
            color: #606d75;
            font-size: .9em;
        }
    }
    .right-box{
        display: flex;
        align-items: flex-end;
        justify-content: flex-end;
        width: 20%;
    }
    
}
.services-card{
    max-width: 900px;
    margin: auto;
    padding-bottom: 100px;

    display: flex;
    flex-wrap: wrap;
    gap: 10px;
}
</style>