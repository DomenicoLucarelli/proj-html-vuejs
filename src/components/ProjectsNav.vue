<script>
export default {

    name: 'ProjectsNav',
    data() {
        return {
            links: [
                {   text: 'All',
                    selected: true
                }, 
                { 
                    text:'Istitutional',
                    selected: false
                  
                }, 
                { 
                    text: 'Social',
                    selected: false

                }, 
                { 
                    text: 'Events',
                    selected: false

                }, 
                { 
                    text: 'Innovation',
                    selected: false

                }, 
                { 
                    text: 'Environment',
                    selected: false

                }, 
                { 
                    text: 'Technology',
                    selected: false

                }
            ]
        }
    },

    methods: {
        isClick(index){

            for(let i = 0; i < this.links.length; i++){
                this.links[i].selected = false
            }
            this.links[index].selected = true
        }
    }
}
</script>

<template>
    <div class="nav">
        <a v-for="(link, index) in links" :key="index" @click="isClick(index)" :style="link.selected == true ? {backgroundColor: '#daeced'} : '' ">{{ link.text }}</a>
    </div>
</template>

<style lang="scss" scoped>

.nav{
    display: flex;
    justify-content: center;
    gap: 20px;

    text-transform: uppercase;

    margin-top: 50px;
    margin-bottom: 30px;
    color: #647a9b;

    a{
        padding: 5px;
        border-radius: 3px;

        cursor: pointer;
    }
}
    
</style>