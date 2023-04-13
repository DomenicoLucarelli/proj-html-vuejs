<script>
import { baseCompile } from '@vue/compiler-core';

export default {
    name: 'AppMessage',
    data() {
        return {
            // variabile booleana che cambia al click del button
            isClick: false,
            // variabili collegate agli input con il v-model
            userName: '',
            userEmail:'',
            userTel:'',
            userInfo:'More Info',
            userMessage:'',
        }
    },

    methods: {
        // funzipne che cambia il valore di isClick
        changeVisibility(){
            // controllo se l'utente non lascia gli input vuoti
            if(this.userName != '' && this.userEmail !='' && this.userTel !='' && this.userInfo !='' && this.userMessage !=''){

                this.isClick = true

               
            }else{
                // se li lascia vuoti compare un alert
                alert('completa tutti i campi per inviare il messaggio')
            }
        },
        // funzione che resetta gli input
        reset(){
            this.isClick = false

            this.userName = ''
            this.userEmail = ''
            this.userTel = ''
            this.userInfo = 'More Info'
            this.userMessage = ''

        }
    },
}
</script>

<template>
    <div class="container">

        <div class="left-box">

            <div class="text-box">

                <h5>Send a message</h5>

                <h2>Get in <mark>Touch</mark></h2>

                <span>We will respond to your message as soon as possible </span>

            </div>

            <form class="input-box" v-if="isClick == false">

                <input type="text" placeholder="Name" v-model="userName" require>

                <input type="email" placeholder="Email" pattern="/^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/" v-model="userEmail" validate="required:true" required>

                <input type="tel" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" placeholder="Phone" v-model="userTel" required>

                <select  v-model="userInfo" >

                    <option selected>More Info</option>

                    <option value="1">One</option>

                    <option value="2">Two</option>

                    <option value="3">Three</option>

                </select>

                <input type="text" size="50" placeholder="Message" v-model="userMessage" required>

            </form>

            <button id="btn" type="submit" class="btn1" @click="changeVisibility()" v-if="isClick == false">SEND</button>

            <div class="alert" v-if="isClick == true">
                <span>

                    Your message has been send.
                </span>

                <button class="btn1" @click="reset()">Send Another message</button>
                
            </div>
            
        </div>

        <div class="right-box">

            <h3>Example Inc.</h3>

            <span>Lorem ipsum dolor sit amet consectetur dipiscing elit</span>

            <span>Praesent diam lacus, dapibus sed imperdient consectetur</span>

            <div class="info-box">
                <div class="tel">
                    <i class="fa-solid fa-phone"></i> <span>+1 (305) 1234-5678</span>
                </div>
                <div class="mail">
                    <i class="fa-solid fa-envelope"></i> <span>hello@example.com</span>
                </div>
                <div class="street">
                    <i class="fa-solid fa-location-dot"></i> <span>Main Avenue 987</span>
                </div>
            </div>

            <button class="btn2 ">VIEW MAP</button>


        </div>
        
    </div>
</template>

<style lang="scss" scoped >

.container{
    max-width: 900px;
    margin: auto;
    min-height: 500px;
    padding: 100px 0;

    display: flex;

    .left-box{
        width: 60%;
        padding: 0 20px;

        .text-box{
            display: flex;
            flex-direction: column;
            gap: 20px;
            h5{
                color: #039f9f;
                text-transform: uppercase;
            }

            h2{
                font-weight: 800;
                color: #21333e;
                font-size: 30px;

            }

            span{
                color: #9f9db2;
                font-size: .9em;
            }   
            
        }
        .alert{
            padding:  50px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            align-items: center;
            justify-content: center;

            span{
                color: #9f9db2;
            }
        }

        .input-box{
            display: flex;
            flex-wrap: wrap;
            gap: 10px;

            padding-top: 30px;

            input,select{
                width: calc(100% / 2 - 10px / 2);
                border: none;
                background-color: #ececec;
                height: 2.5em;
                border-radius: 3px;
                padding: .3em .8em;

                &:last-child{
                    flex-grow: 1;
                    padding: 1em .8em 100px .8em;
                    margin-bottom: 20px;
                       
                }      
            }
            select{
                color: #6d6d6d;
                
            }
        }

        
    }

    .right-box{
        width: 40%;
        display: flex;
        flex-direction: column;
        gap: 10px;

        padding: 0 20px;

        h3{
            color:#21333e ;
        }

        span{
            color: #9f9db2;
            font-size: .9em;

        }

        .info-box{
            display: flex;
            flex-direction: column;
            gap: 15px;
            padding: 20px 0;
            
            span{
                color:#058283 ;
                font-size: .9em;
                padding-left: 5px;
            }

            .fa-solid{
                background-color: #daeced;
                color: #058283;
                padding: 10px;
                border-radius: 50%;
            }
        }
        
        .btn2{
            align-self: flex-start;
        }
    }

}
    
</style>