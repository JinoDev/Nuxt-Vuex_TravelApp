<template>
    <NuxtLink :to="`/packages/${card.id}`"  class="card-container">
<img :src="require(`@/assets/images/${card.image || 'lisbon.jpeg'}`)" alt="travel dest" class="image">
    </NuxtLink>
</template>

<script>
    export default {
        props: ['card']
    }
</script>

<style scoped>
.card-container {
        width: 25%;
        height: 12.5rem;
        overflow: hidden;
        cursor: pointer;
    }
    .image {
        width: 200px;
        height: 100px;
        border-radius: 0.5rem;
    }
</style>