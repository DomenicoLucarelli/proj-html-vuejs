<script>
export default {

    name: 'NetworkCard',

    data() {
        return {
            
        }
    },

    props: {
        image: String,
        title: String,
        info: String,
    }
}
</script>

<template>
    <div class="card">
        <div class="top">
            <i :class="image"></i>
            <h3>{{title}}</h3>
        </div>

        <div class="middle">
            {{ info }}
        </div>
        
    </div>
</template>

<style lang="scss" scoped >
.card{
    width: calc(100% / 2 - 10px / 2 );
}
.top{
    display: flex;
    gap: 5px;
    align-items: center;

    i{
        color: #03a8ac;
    }

    h3{
        color: white;
    }

}

.middle{
    font-size: .9em;
    color: #606d75;
}
    
</style>