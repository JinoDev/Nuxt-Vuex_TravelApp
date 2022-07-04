<template>
  <div class="container">
    <MyTrip
     v-for="trip in myTrips"
     :key="trip.id"
     :trip="trip"
      />
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  layout: "no-nav",
  computed: {
    ...mapState(["myTrips"]),
  },
};
</script>

<style scoped></style>
