<script>
export default {

    name: 'ProjectsCard',

    data() {
        return {

            isHover: false
        }
    },

    props:{
        img: String,
        title: String,
        text: String,
        back: String,
    },

    methods: {

        hoverChange(){

            this.isHover = !this.isHover  
           
        },

        
    },
}
</script>

<template>
    <div class="card" :style="{backgroundImage: 'url('+ img +')'}" @mouseover="hoverChange()" @mouseleave="hoverChange()">

        <div class="text-container" :class="back">

            <h3>{{ title }}</h3>

            <span v-if="isHover == true">{{ text }}</span>

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
       
        &:hover h3{
            transform: translateY(-50px);
            transition: 1s linear;
        }
        &:hover span{
            transform: translateY(-50px);
            transition: 1s linear;
        }

    }
    h3{
        color: white;
        
    }
    span{
        color: #b9b8b9;
        font-size: .9em;
        
    }

    
}
    
</style>