<template>
    <div class="container">
<h3 class="header">
    {{cardsSection.title }}
</h3>
<div class="card-container">
<SmallCard
v-for="card in cardsSection.cards"
:key="card.id"
:card="card"
/>
</div>
    </div>
</template>

<script>
    export default {
        props: ['cardsSection']
    }
</script>

<style scoped>
.container {
        padding: 2rem 0;
        margin-bottom: -2.5rem;
    }
    .header {
        font-weight: 700;
        font-size: 1.5rem;
        margin-top: 1rem;
        margin-bottom: 3rem;
        margin-left: 2rem;
        color: rgb(124, 124, 124);
        font-size: 1rem;
    }
    .card-container {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }
</style>