<script>
import NetworkCard from './NetworkCard.vue';

export default {
    name: "AppNetwork",
    data() {
        return {
            // array di oggetti per le cards
            cards: [
                {
                    image: "fa-solid fa-medal",
                    title: "Tradition",
                    des: "Lorem ipsum dolor sit amet consectetur dipiscing elit",
                },
                {
                    image: "fa-solid fa-lock",
                    title: "Securety",
                    des: "Lorem ipsum dolor sit amet consectetur dipiscing elit",
                },
                {
                    image: "fa-regular fa-pen-to-square",
                    title: "Certificare",
                    des: "Lorem ipsum dolor sit amet consectetur dipiscing elit",
                },
                {
                    image: "fa-solid fa-graduation-cap",
                    title: "Expertise",
                    des: "Lorem ipsum dolor sit amet consectetur dipiscing elit",
                },
            ],
        };
    },
    components: { NetworkCard }
}
</script>

<template>

    <div class="ext-container">

        <img class="bullets1" src="img/bullets.png" alt="">

        
        <div class="container">
            
    
            <div class="left-section">
    
                <div class="inner-content">
                    <h5>About The Network</h5>
            
                    <div class="title">
            
                        <h1><mark>The </mark> Company </h1>
            
                    </div>
            
                    
                    <p>
                        For 12 years we have been providing audit and warranty, financial advice, 
                        risk advice; taxes and related services for select clients
                    </p>
                    
                    <div class="card-container">
                        <!-- creo tante card quanti sono gli elementi di cards e passo al componente NetworkCard le informazioni tramite props -->
                        <NetworkCard v-for="(card, index) in cards" :key="index" :image="card.image" :title="card.title" :info="card.des"></NetworkCard>
    
                    </div>
    
                    <div class="btn-container">
                        <div class="btn1">Get in touch</div>
                        <div class="btn2">Read More</div>
                    </div>
                </div>
    
    
            </div>
    
            <div class="right-section">
    
                <img src="img/about-4.jpg" alt="">
    
            </div>
    
    
        </div>

        <img class="bullets2" src="img/bullets.png" alt="">


    </div>
    

</template>

<style lang="scss" scoped >

.ext-container{
    position: relative;

    .bullets1{
        width: 100px;
        
        position: absolute;
        top: 0;
        left: 50%;
        transform: translate(-50% , -50%);
        opacity: 0.8;
    }

    .bullets2{
        width: 100px;
        
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translate(-50% , 50%);
        opacity: 0.8;


    }
}
    .container{
        
        background-color: #111117;
        
        display: flex;
        
        
        
        .left-section{
            width: 50%;
            align-self: center;

            .inner-content{
                width: 70%;
                margin-left: auto;

                padding: 100px 20px 100px 0;

                display: flex;
                flex-direction: column;
                gap: 20px;

                h5{
                    text-transform: uppercase;
                    color: #0dabb2;
                }

                .title {
                    color: white;

                    mark{
                        color: white;
                        background-color: #0e272d;
                    }
                }

                p{
                    color: #b0c3c4;
                    font-size: .9em;
                }

                .card-container{
                    display: flex;
                    flex-wrap: wrap;
                    gap: 10px;

                    padding: 50px 0;
                }

                .btn-container{
                    display: flex;
                    gap: 20px;

                    .btn2{
                        background-color: transparent;
                        color: white;
                    }
                }

            }
        }

        .right-section{
            width: 50%;

            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }
    }
</style>