<template>
  <Navbar />
  <Landing />
  <Description />
  <Offer />
</template>

<script>
import Navbar from "./components/Nav"
import Landing from "./components/Landing"
import Description from "./components/Description"
import Offer from "./components/Offer"

import AOS from "aos";
import "aos/dist/aos.css"

export default {
  name: 'App',
  components: {
    Navbar,
    Landing,
    Description,
    Offer
  },
  created(){
    AOS.init();
  }
}
</script>

<style>
body{
  background: url("./assets/bg.jpg");
  background-repeat: no-repeat;
}
*{
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
  font-family: 'Roboto', sans-serif;
}


</style>
