<script>
import ProjectsCard from './ProjectsCard.vue';
import ProjectsNav from './ProjectsNav.vue';

export default {
    name: "AppProjects",
    data() {
        return {
            cards: [
                {
                    image:'img/project-1.jpg',
                    title:'Academic professional program in social media',
                    des: 'lorem ipsum dolor sit amet consectetur dipiscing elit',
                },

                {
                    image:'img/project-2.jpg',
                    title:"President's speech at the annual meeting" ,
                    des: 'lorem ipsum dolor sit amet consectetur dipiscing elit', 
                },

                {
                    image:'img/project-3.jpg',
                    title:'International trip business in shanghai',
                    des: 'lorem ipsum dolor sit amet consectetur dipiscing elit', 
                },

                {
                    image:'img/project-4.jpg',
                    title:'Technology workshop with education theme',
                    des: 'lorem ipsum dolor sit amet consectetur dipiscing elit', 
                },

                {
                    image:'img/project-5.jpg',
                    title:'Donation of clothes and food to the partner NGO',
                    des: 'lorem ipsum dolor sit amet consectetur dipiscing elit', 
                },

                {
                    image:'img/project-6.jpg',
                    title:'Confraternization of the procurament team',
                    des: 'lorem ipsum dolor sit amet consectetur dipiscing elit', 
                },
            ]
        };
    },
    components: { ProjectsNav, ProjectsCard }
}
</script>

<template>
    <div class="container">

        <h5>We do more for everyone</h5>

        <h2>Actions & <mark>Projects</mark></h2>

        <ProjectsNav></ProjectsNav>

        <div class="cards-container">

            <ProjectsCard v-for="(card, index) in cards" :key="index" :img="card.image" :title="card.title"></ProjectsCard>

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
    
</style>