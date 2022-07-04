<template>
    <div class="trip-container">
        <img :src="require(`@/assets/images/${trip.image}`)" alt="city/trip image">
        <div class="text-container">
            <h4> {{trip.title}} </h4>
            <p> {{trip.description}} </p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['trip']
    }
</script>

<style scoped>
    .trip-container {
        display: flex;
        margin: 3rem 0
    }
    .text-container {
        padding: 0 1rem
    }
    img {
        width: 17.5rem;
        border-radius: 0.5rem;
        height: 11rem
    }
    p {
        font-size: 0.8rem;
        color: grey
    }
</style>