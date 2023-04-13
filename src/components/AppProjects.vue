<script>
import ProjectsCard from './ProjectsCard.vue';
import ProjectsNav from './ProjectsNav.vue';
import {store} from '../store.js'

export default {
    name: "AppProjects",
    data() {
        return {
            store,
            // array di oggetti per le cards
            cards: [
                {
                    image:'img/project-1.jpg',
                    title:'Academic professional program in social media',
                    des: 'Lorem ipsum dolor sit amet consectetur dipiscing elit',
                    correspondence:[0,2] ,
                },

                {
                    image:'img/project-2.jpg',
                    title:"President's speech at the annual meeting" ,
                    des: 'Lorem ipsum dolor sit amet consectetur dipiscing elit',
                    correspondence:[0,4], 
                },

                {
                    image:'img/project-3.jpg',
                    title:'International trip business in shanghai',
                    des: 'Lorem ipsum dolor sit amet consectetur dipiscing elit',
                    correspondence:[0,5] , 
                },

                {
                    image:'img/project-4.jpg',
                    title:'Technology workshop with education theme',
                    des: 'Lorem ipsum dolor sit amet consectetur dipiscing elit',
                    correspondence:[0,6], 
                },

                {
                    image:'img/project-5.jpg',
                    title:'Donation of clothes and food to the partner NGO',
                    des: 'Lorem ipsum dolor sit amet consectetur dipiscing elit',
                    correspondence:[0,1], 
                },

                {
                    image:'img/project-6.jpg',
                    title:'Confraternization of the procurament team',
                    des: 'Lorem ipsum dolor sit amet consectetur dipiscing elit',
                    correspondence:[0,3], 
                },
            ]
        };
    },
    components: { ProjectsNav, ProjectsCard },

    
}
</script>

<template>
    <div class="container">

        <h5>We do more for everyone</h5>

        <h2>Actions & <mark>Projects</mark></h2>

        <ProjectsNav></ProjectsNav>

        <div class="cards-container">
            <!-- creo tante card quanti sono gli elementi dell'array cards passo le info tramite props e passo la classe active solo alle card che hanno nelle correspondence un valore uguale al'indice dell'elemento cliccato in ProjectsNav -->
            <ProjectsCard v-for="(card, index) in cards" :key="index" :img="card.image" :title="card.title" :text="card.des" :back="card.correspondence.includes(store.navIndex) ? 'active' : 'not-active'"></ProjectsCard>

        </div>
    </div>
</template>

<style lang="scss" scoped >

.container{
    width: 900px;
    margin: 100px auto;
    text-align: center;

    h5{
        text-transform: uppercase;
        color: #0dabb2;
        padding: 10px 0;
    }

    h2{
        font-weight: 800;
        color: #21333e;
        font-size: 30px;
    }

    .cards-container{
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }
}

.active{
    background-color: black;
}
    
</style>