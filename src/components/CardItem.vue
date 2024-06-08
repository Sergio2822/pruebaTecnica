<template>
  <div class="cards-container">
    <div v-for="card in cards">
      <img :src="card.imageUrl" />
      <p>Name: {{ card.name }}</p>
      <p>Color: {{ card.colors }}</p>
      <p>Type: {{ card.type }}</p>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    cards: {
      type: Object,
    },
  },
});
</script>
<style scoped>
.cards-container {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  gap: 10px;
}
</style>
