<script>
export default {
    name: 'AppSponsor',
    data() {
        return {
            // creo un array di immagini
            sponsor: ['logo-4.png', 'logo-5.png', 'logo-1.png', 'logo-2.png', 'logo-3.png', 'logo-4.png',]
        }
    },
}
</script>

<template>
    <div class="container">

        <div class="sponsor">
            <!-- creo tanti tag img quanti sono gli elementi dell'array -->
            <img  v-for="(item, index) in sponsor" :key="index" :src=" 'img/' + item" alt="">
        </div>
        
    </div>
</template>

<style lang="scss" scoped>
    .container{
        background-color: #111117;
        min-height: 200px;

        display: flex;
        align-items: center;
        
        .sponsor{

            max-width: 900px;
            margin: auto;

            display: flex;
            gap: 50px;

            img{
                width: 80px;
                object-fit: contain;
                filter: invert(100%);
            }


        }
    }
</style>