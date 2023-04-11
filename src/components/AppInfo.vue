<script>
export default {

    name: 'AppInfo',

    data() {
        return {
            
        }
    },
}
</script>

<template>
    <div class="info">

        <div class="container">
            <div class="left-section">

                <i class="fa-solid fa-clock"></i> <span>Open Hour: Mon-Sat-9:00-18:00</span>

            </div>

            <div class="right-section">

                <div class="tel">
                    <i class="fa-solid fa-phone"></i> <span>+1(305)1234-5678</span>
                </div>

                <div class="mail">
                    <span>hello@example.com</span>
                </div>

                <div class="social">

                    <i class="fa-brands fa-facebook-f"></i>

                    <i class="fa-brands fa-twitter"></i>

                    <i class="fa-brands fa-linkedin-in"></i>

                </div>

            </div>
            
        </div>
        
    </div>
</template>

<style lang="scss" scoped>
    
    .info{
    
        background-color: #0d1b2a;
        padding: 5px 0;

        color: #e2e3e7;
        font-size: .8em;

        .container{

            display: flex;
            justify-content: space-between;
            
            max-width: 1100px;
            margin: auto;

            .right-section{
                
                display: flex;
                gap: 30px;
                

                .social{
                    display: flex;
                    align-items: center;
                    gap: 30px;

                }
            }
        }
    }

</style>