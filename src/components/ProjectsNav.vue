<script>
import { store } from '../store'

export default {

    name: 'ProjectsNav',
    data() {
        return {
            store,
            // array di oggetti links
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
        // funzione che passa l'index del link
        isClick(index){
            // ciclo che mette in false tutti i selected
            for(let i = 0; i < this.links.length; i++){
                this.links[i].selected = false
            }
            // cambio il selected dell'elemento cliccato
            this.links[index].selected = true
            // passo l'index dell'elemento cliccato alla variabile navIndex presente in store
            store.navIndex = index
            
        }
    }
}
</script>

<template>
    <div class="nav">
        <!-- inserisco tutti i link e applico lo stile solo al link con selected = true -->
        <a v-for="(link, index) in links" :key="index" @click="isClick(index)" :style="link.selected == true ? {backgroundColor: '#daeced'} : '' " >{{ link.text }}</a>
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