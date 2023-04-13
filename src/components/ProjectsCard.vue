<script>
export default {

    name: 'ProjectsCard',

    data() {
        return {
            
         
        }
    },
    // predispongo le props
    props:{
        img: String,
        title: String,
        text: String,
        back: String,
    },

    
}
</script>

<template>
    <!-- passo l'immagine di background tramite props -->
    <div class="card" :style="{backgroundImage: 'url('+ img +')'}">

        <div class="text-container" :class="back">

            <h3>{{ title }}</h3>
            <!-- la props text viene visualizzata solo quando isHover è true -->
            <span >{{ text }}</span>

        </div>
        
    </div>
</template>

<style lang="scss" scoped >

.card{
    width: calc(100% / 3 - 20px / 3 * 2);
    height: 300px;
    
    background-size: cover;

    border-radius: 10px;
    overflow: hidden;
    cursor: pointer;

    .active{

        background-color: rgba(0, 0, 0, 0.329);
    }

    .not-active{
        
        background-color: rgba(0, 0, 0, 0.692);

    }
    .text-container{

        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content:flex-end;
        
        padding: 20px;
        font-weight: bold;
        
        position: relative;
       
        &:hover h3{
            transform: translateY(-50px);
            transition: 1s ease;
        }
        &:hover span{
            transform: translateY(-50px);
            transition: 1s ease;
        }

    }
    h3{
        color: white;
        position: absolute;
    }
    span{
        color: #b9b8b9;
        font-size: .9em;
        position: absolute;
        bottom: -40px;
        
    }

    
}
    
</style>