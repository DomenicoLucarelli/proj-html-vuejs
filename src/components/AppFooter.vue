<script>
import FooterCard from './FooterCard.vue';
import {store} from '../store.js'
export default {
    name: "AppFooter",
    data() {
        return {
            
            links: [
                
                { 
                    title: 'About',
                    list:  ['The Company','Istitutional', 'Social & Events', 'Innovation', 'Environment', 'Technology',],
                },

                {
                    title: 'Services',
                    list: ['Audit & Assurance', 'Financial Advisory', 'Analytics M&A', 'Middle Marketing', 'Legal Consulting', 'Regulatory Risk',],
                },

                {
                    title: 'Support',
                    list: ['Responsibility', 'Terms of Use', 'About Cookies', 'Privacy Policy', 'Accessibilty', 'Information',]
                }
            
            ]

        };
    },
    components: { FooterCard }
}
</script>

<template>
    <div class="container">

        <div class="footer-box">


            <div class="info">
                <img src="img/svg-7.svg" alt="">

                <span>A functional HTML Template for corporate & Business</span>

                <div class="tel">

                    <i class="fa-solid fa-phone"></i> <span>+1 (305) 1234-5678</span>

                </div>

                <div class="mail">

                    <i class="fa-solid fa-envelope"></i> <span>hello@example.com</span>

                </div>

                <div class="street">

                    <i class="fa-solid fa-location-dot"></i> <span>Main Avenue 987</span>

                </div>

                <button class="btn2">Get in touch</button>
            </div>

            <div class="footer-cards">

                <FooterCard v-for="(link, index) in links" :key="index" :title="link.title" :items="link.list"></FooterCard>

            </div>

        </div>
        
    </div>

    <div class="bottom-footer">
        <div class="box">
            <span>Enjoy the low price. We are tracking any intention of piracy</span>
            <span>NexGen is Proudly Powered by <span style="color: #085b5d;">Coding</span> </span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .container{
        
        background-color: #111117;
        

        .footer-box{
            max-width: 900px;
            margin: auto;
            padding: 100px 0;
            display: flex;
            
            .info{
                width: 30%;
                display: flex;
                flex-direction: column;
                gap: 10px;
                color: #c0c3d0;
                font-size: .9em;
                

                img{
                    width: 120px;
                    margin-bottom: 20px;
                }

                .tel{
                    margin-top: 20px;
                }

                .btn2{
                    align-self: flex-start;
                    background-color:#111117 ;
                    color: white;
                    margin-top: 20px;
                }
            }

            .footer-cards{
                width: 70%;
                display: flex;
                gap: 15px;
            }
        }

    }

    .bottom-footer{
        height: 50px;
        background-color: #0d0d11;
        display: flex;
        align-items: center;
        


        .box{
            max-width: 900px;
            margin: auto;
            width: 100%;

            display: flex;
            justify-content: space-between;

            color:#c0c3d0 ;
            font-size: .9em;

        }
    }
</style>