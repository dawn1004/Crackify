<template>
    <div 
    class="contact" 
    v-if="dialog"
    data-aos="fade-up"
    data-aos-duration="300"
    >
        <div class="arrow" @click="hideModal">
            <img src="../assets/arrow.png" alt="">
        </div>

        <form 
        class="form"
        @submit.prevent="sendEmail">
            <h1>Leave Your Email Here</h1>
            <p>To order please send your email and our team will go to you as soon as possible. Or contact us on our official Facebook page  <a href="https://www.facebook.com/Crackify-Software-110190294190470/?notif_id=1602181905975117&notif_t=page_fan&ref=notif">@Crackify_Software</a> </p>
            
            <input 
            type="text" 
            placeholder="Email"
            v-model='userEmail'
            class="email"
            name="email"
            >
            <button type="submit">Send Order</button>

        </form>
    </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
    name: "Contact",
    props:{
        dialog: Boolean
    },
    data() {
        return {
            userEmail: ""
        }
    },
    methods: {
        sendEmail(e){
            if(this.userEmail!=""){
                emailjs.sendForm('gmail', 'template_m9u6wth', e.target, 'user_gKk0ht4Px3wBD7UyrOG0B')
                    .then((result) => {
                        alert("Email Sent")
                        console.log('SUCCESS!', result.status, result.text);
                        this.userEmail =""
                    }, (error) => {
                        console.log('FAILED...', error);
                    });
            }else{alert("please fill info")}
        },
        hideModal(){
            this.$emit('hide-modal', false)
        }
    },
}
</script>

<style lang="scss">
.contact{
    position: fixed;
    top: 0px;
    left: 0px;
    height: 100vh;
    width: 100vw;
    background: white;
    z-index: 2;
    .arrow{
        position: absolute;
        top: 10px;
        left: 10px;
        width: 40px;
        img{
            width: 100%;
            transform: scaleX(-1);
        }
    }
    .form{
        position: absolute;
        top: 50%;
        transform: translate(0%, -50%);
        display: flex;
        flex-direction: column;
        // background: red;
        // justify-content: space-around;
        align-items: center;
        width: 100%;
        h1{
            font-size: 72px;
            text-align: center;
        }
        p{
            font-size: 18px;
            margin-top:10px;
            max-width: 800px;
            text-align: center;
            a{
                text-decoration: none;
                color: #0a274a;
            }
        }
        input{
            width: 600px;
            font-size: 50px;
            border: 0.5px solid rgba(0, 0, 0, 0.171);
            margin-top: 40px ;
            padding: 10px;

        }
        input:focus::placeholder {
            color: transparent;
        }
        button{
            width: 400px;
            font-size: 40px;
            border: none;
            padding: 10px;
            margin-top: 20px ;
            background: #0A274A;
            color: white;
        }
    }
}


@media only screen and (max-width: 500px) {
.contact{
    .form{
        h1{
            font-size: 38px;
            text-align: center;
        }
        p{
            font-size: 14px;
            margin-top:10px;
        }
        input{
            width: 300px;
            font-size: 28px;
        }
        button{
            width: 250px;
            font-size: 26px;
        }
    }
}
}
</style>