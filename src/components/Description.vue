<template>
    <div 
    class="description-container"
    data-aos="fade-up"
    data-aos-duration="1000"
    >
        <div class="description">
            <h1>What we offer?</h1>
            <p>We offer the most affordable bundle of popular software applications that you can install easily in your personal computers or laptop.</p>
            <!-- <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Reprehenderit excepturi sint numquam quas aliquam? Veniam perferendis libero nemo, aliquid quasi molestias quos doloremque rerum excepturi iusto. Molestias qui itaque placeat. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Reprehenderit excepturi sint numquam quas aliquam? Veniam perferendis libero nemo, aliquid quasi molestias quos doloremque rerum excepturi iusto. Molestias qui itaque placeat.</p> -->
        </div>

    </div>
</template>

<script>
export default {
    name: "Description",
}
</script>

<style scoped>
.description-container{
    margin: 100px;
    margin-top: 200px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.description-container h1{
    font-size: 38px;
    letter-spacing: 2px;
    margin-bottom: 20px;
    color: #0A274A;
}

.description-container p{
    font-size: 26px;
    text-align: justify;
    color: rgb(41, 41, 41);
}


@media only screen and (max-width: 500px) {
    .description-container{
        margin: 45px;
        margin-top: 140px;
    }
    .description-container h1{
        font-size: 28px;
    }
    .description-container p{
        font-size: 18px;
    }

}
</style>