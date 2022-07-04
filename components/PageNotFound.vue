<template>
    <div>
        <h1>Page Not Found</h1>
        <img :src="require('@/assets/images/404.jpeg')" alt="404 page not found">
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    div {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 50rem
    }
    h1 {
        font-size: 3rem;
        color: #a23447;
    }
    img {
        width: 25rem;
        margin: 0 auto
    }
</style>