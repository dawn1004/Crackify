<template>
    <div class="navbar">
        <img src="../assets/logo.png" alt="">
    </div>
</template>

<script>
export default {
    name: "Navbar"
}
</script>
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
<style scoped>
    .navbar{
        height: 60px;
        display: flex;
        align-items: center;
    }
    .navbar img{
        height: 70%;
        margin: 100px
    }

    @media only screen and (max-width: 500px) {
    .navbar{
        height: 50px;
    }
    .navbar img{
        margin: 30px
    }
    }
</style>