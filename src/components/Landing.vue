<template>
    <div 
    class="landing"
    data-aos="fade-in"
    data-aos-duration="1000
    >
        <div 
        class="left"
        data-aos="fade-right"
        data-aos-duration="500"
        >
            <h1>Crackify Softwares</h1>
            <h3>Affordable application bundle??</h3>
            <button @click="showDialog">Buy now...</button>
        </div>
        <div 
        class="right"
        :data-aos="state.screenWidth >=500 ? 'fade-up' : '' "
        data-aos-duration="500"
        >
            <img src="../assets/right.png" alt="">
        </div>
    </div>

    <Contact :dialog="state.dialog" @hide-modal="hide"/>
</template>

<script>
import Contact from "./Contact"

import { reactive } from 'vue'

export default {
    name: "Landing",
    components:{
        Contact
    },
    setup(){
        const state = reactive({
            dialog: false,
            screenWidth: window.innerWidth,
        })

        function showDialog(){
            state.dialog =true
        }
        function hide(){
            state.dialog =false
        }
        return{state, showDialog, hide}
    }
}
</script>

<style scoped>


.landing{
    display: flex;
    /* background: red; */
    margin-left: 100px ;
    margin-right: 100px ;
    justify-content: space-between;
    height: 90vh;
    align-items: center;
    
}

.landing .left{

}
.landing .right{
    
}

.landing .right img{
    width: 440px;
}
.landing .left h1{
    font-size: 66px;
    color: #0A274A;
    letter-spacing: 1px;
}

.landing .left h3{
    font-size: 32px;
    color: #656565;
    letter-spacing: 2px;
    font-weight: 400;
}

.landing .left button{
    width: 270px;
    background: #0A274A;
    border: none;
    font-size: 26px;
    color: rgb(245, 245, 245);
    letter-spacing: 1px;
    padding: 10px 0px;
    margin-top: 30px;
}
.landing .left button:hover{
    opacity: 0.9;
}

@media only screen and (max-width: 500px) {
    .landing{
        flex-direction: column;
        margin-left: 45px ;
        margin-right: 30px ;
        justify-content: space-around;
        /* background: red; */
        height: 550px;
        margin-top: 30px;

    }
    .landing .right img{
        width: 270px;
        margin-left: -40px;
    }
    .landing .left h1{
        font-size: 48px;
    }

    .landing .left h3{
        font-size: 22px;
    }

    .landing .left button{
        width: 180px;
        font-size: 18px;
    }
}
</style>
