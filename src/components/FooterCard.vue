<script>

export default {

    name: 'FooterCard',
    data() {
        return {
            
             
            
        }
    },
    // predispongo le props che mi verranno passate da AppFooter
    props: {
        title: String,
        items: Array,
    }
}
</script>

<template>
    <div class="card">
        <div class="title">
            <!-- passo la props title -->
            <h2>{{ title }}</h2>
        </div>

        <ul>
            <!-- creo un ciclo per ogni elemento presente nella props items che è un array e visualizzo i suoi elementi -->
           <li v-for="(item, index) in items" :key="index"> <i class="fa-solid fa-chevron-right"></i> {{ item }}</li>
          
        </ul>

        
    </div>
</template>

<style lang="scss" scoped>
    .card{
        width: calc(100% / 3 - 15px / 3 * 2);
        min-height: 100px;

        background-color: #19191f;
        
        padding: 1.5em 1.2em;

        border-radius: 10px;

        h2{

            color: white;
            padding-bottom: 5px;
        }

        li{
            color: #a9a79e;
            font-size: .9em;
            padding: 5px 0;
            font-weight: 600;
            cursor: pointer;

            &:hover{
                background-color:rgba(255, 255, 255, 0.178);
                border-radius: 3px;
            }
        }
    }
</style>