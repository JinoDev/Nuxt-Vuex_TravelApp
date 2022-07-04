<template>
    <div class="hero container">
<div class="text-container">
    <h1 class="header">Find your next Destination</h1>
<p class="snippet">This website features all of the information you need to plan your next trip.</p>
<button class="button btn">Start Looking</button>
</div>
<img src="~assets/wanderlust.jpeg" alt="travel picture" class="image">
    </div>
</template>

<script>
    export default {
     
        }
</script>

<style scoped>

   .hero {
        height: 50vh;
        position: relative;
        display: flex;
        padding: 5rem 0;
        margin-top: -2rem;
        margin-bottom: 18rem;
        align-items: flex-start;
        justify-content: space-between;
    }
    .text-container {
        width: 50%;
        margin-top: 4rem;
        font-family: Arial, Helvetica, sans-serif;
    }
    .header {
        color: rgb(40, 49, 76);
        font-size: 5rem;
    }
    .snippet {
        color: rgb(79, 78, 78);
        font-size: 1.25rem;
        margin-bottom: 2rem;
    }
    .image {
        width: 24.5rem;
        margin-top: 5rem;
        border-radius: 50%;
        border: 1px solid #99FEFF;
    }
    .overlay {
        background: rgba(0, 0, 0, 0);
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
    }
    .button {
        padding: 1rem 4rem;
        border-radius: 50px;
        background-color: #B983FF;
        color: #ffffff;
        width: 18rem;
        font-weight: 900;
    }
    @media (max-width: 500px) {
        .hero {
            height: 40vh;
        }
    }
</style>