<template>
  <NuxtLink :to="`/packages/${card.id}`" class="card">
    <img
      :src="require(`@/assets/images/${card.image || 'tbilisi.jpeg'}`)"
      alt="travel destination"
      class="image"
    />
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </NuxtLink>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped>
.card {
  width: 30%;
  height: 28rem;
  border: none;
  overflow: hidden;
  cursor: pointer;
  padding: 2rem;
  background-color: #effffd;
  border-radius: 0.5rem;
  margin-bottom: 1.5rem;
  border-radius: 15px;
  background: linear-gradient(315deg, #ffffff, #d7e6e4);
  box-shadow: -31px -31px 62px #deedeb, 31px 31px 62px #ffffff;
}
  .card:hover {
    text-decoration: none;
  }
.image {
  height: 50%;
  border-radius: 0.5rem;
  margin-bottom: 2rem;
}
.header {
  color: black;
  font-size: 1.15rem;
  margin-top: 0.4rem;
}
.snippet {
  color: rgb(79, 78, 78);
  margin-bottom: 2rem;
}
.header:hover, .snippet:hover {
color: rgb(89, 44, 44);
}
</style>
