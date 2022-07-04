<template>
  <div class="container">
    <b-button id="show-btn" @click="showModal">Book Trip</b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="calendar-container">
        <div class="text-container">
          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Impedit
            dolore rerum quo error quis, explicabo eaque nobis corporis expedita
            itaque porro debitis modi labore, laudantium nihil minus perferendis
            fugit dignissimos adipisci molestias velit assumenda magnam ipsum
            quasi? Reprehenderit, consectetur quam!
          </p>
        </div>
        <vc-date-picker :value="null" color="indigo" is-dark is-range />
      </div>
      <b-button
        id="show-btn"
        @click="
          () => {
            addTrip(pack.id);
            hideModal();
          }
        "
      >
        Checkout
      </b-button>
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from "vuex";
export default {
  props: ["pack"],
  methods: {
    showModal() {
      this.$refs["my-modal"].show();
    },
    hideModal() {
      this.$refs["my-modal"].hide();
    },
    toggleModal() {
      this.$refs["my-modal"].toggle("#toggle-btn");
    },
    ...mapMutations(["addTrip"]),
  },
};
</script>

<style scoped>
button {
  border: none;
  padding: 0.7rem 2.5rem;
  border-radius: 5px;
  background-color: #9ba3eb;
  color: #fff;
}
button:hover {
  color: #fff;
  background-color: #1f2b1f;
}
p {
  color: grey;
}
.text-container {
  padding: 0.5rem;
}
.calendar-container {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
</style>
