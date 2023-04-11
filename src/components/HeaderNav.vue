<script>
export default {

    name: 'HeaderNav',
    data() {
        return {
            
            links : ['Home', 'Services', 'About', 'Projects', 'Results'],
        }
    },
}
</script>

<template>
    <div class="nav">

        <div class="logo">
            <img src="img/logo.PNG" alt="">
        </div>

        <div class="dx-nav">

            <div class="links">
                <a :href="'#' + link " v-for="(link, index) in links" :key="index">{{ link }}</a>
            </div>
    
            <button class="btn1">Get in touch</button>

        </div>
        
    </div>
</template>

<style lang="scss" scoped>

.nav{
    display: flex;
    justify-content: space-between;

    max-width: 900px;
    margin: 0 auto ;
    margin-top: 10px;

    
    .logo{
        img{
            
            width: 100px;
        }
    }
    .dx-nav{
        display: flex;
        gap: 20px;
        .links{
            display: flex;
            align-items: center;
            gap: 20px;
            
            text-transform: uppercase;
            font-size: .8em;
        }

        
        
    }


}
    
</style>