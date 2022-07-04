<template>
  <div class="container">
    <h4 class="header">
      {{ cardsSection.title }}
    </h4>
    <p class="snippet">
      {{ cardsSection.snippet }}
    </p>
    <div class="cards-container">
      <LargeCard
        v-for="card in cardsSection.cards"
        :key="card.id"
        :card="card"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: ["cardsSection"],
};
</script>

<style scoped>
.container {
  margin-top: 8rem;
}
.header {
  font-weight: 700;
  font-size: 1.5rem;
  color: rgb(40, 49, 76);
  margin-top: -9rem;
  margin-bottom: 2rem;
}
.snippet {
  color: rgb(79, 78, 78);
  margin-bottom: 3rem;
}
.cards-container {
  display: flex;
  justify-content: space-between;
}
</style>
