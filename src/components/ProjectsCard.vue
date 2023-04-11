<script>
export default {

    name: 'ProjectsCard',

    data() {
        return {
            
        }
    },

    props:{
        img: String,
        title: String,
        text: String,
    }
}
</script>

<template>
    <div class="card" :style="{backgroundImage: 'url('+ img +')'}">

        <div class="text-container">

            <h3>{{ title }}</h3>

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

    .text-container{

        height: 100%;
        display: flex;
        align-items:flex-end;
        background-color: rgba(0, 0, 0, 0.479);
        padding-bottom: 20px;

    }
    h3{
        color: white;
    }

    
}
    
</style>