<script>
export default {

    name: 'ServicesCard',

    data() {
        return {
            
        }
    },

    props: {
        img: String,
        title: String,
        info: String
    }
}
</script>

<template>
    <div class="card">

        <div class="card-top">

            <img :src="img" alt="">

            <div class="arrow-box">

                <i class="fa-solid fa-arrow-right"></i>

            </div>

        </div>

        <div class="card-title">
            
           <h3> {{ title }}</h3>
        
        </div>

        <div class="card-description">{{ info }}</div>
        
    </div>
</template>

<style lang="scss" scoped >
    .card{

        width: calc(100% / 3 - 10px / 3 * 2);
        padding: 40px;
        border-radius: 20px;
        background-color: white;

        display: flex;
        flex-direction: column;
        gap: 10px;
        .card-top{
            display: flex;
            justify-content: space-between;

            img{
                width: 30px;
                
            }

            .arrow-box{
                display: flex;
                align-items: center;
                justify-content: center;
                
                padding: 5px;
                border-radius: 50%;
                width: 30px;
                cursor: pointer;

                &:hover {
                    background-color: #81d3d3;
                }
            }

            .fa-solid{
                color: #81c1c1;
                font-size: 1.4em;
                

                &:hover{
                    color: #058283;
                    
                }
            }
        }

        .card-title{
            color: #1f303c;
        }

        .card-description{
            color: #606d75;
            font-size: .9em;
        }
    }
</style>