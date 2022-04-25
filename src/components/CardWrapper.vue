<script setup>
import Card from "./Card.vue";
const props = defineProps({
  items: {
    type: Array,
    required: true,
  },
  disabled: {
    type: Boolean,
    required: false,
    default: false
  },
});
</script>

<template>
  <div class="card-wrapper">
    <Card
      v-for="(item, index) in props.items"
      :key="index"
      :title="item.title"
      :variant="item.variant"
      :duration="item.duration"
      :color="item.color"
      :contentType="item.contentType"
      :presenter="item.presenter"
      :presenter_url="item.presenter_url"
      :newContent="item.newContent"
      :disabled="disabled"
      :href="item.href"
    />
  </div>
</template>

<style scoped>
.card-wrapper {
  width: calc(100% + 30px);
  display: flex;
  overflow-x: scroll;
  -webkit-overflow-scrolling: touch;
  -ms-overflow-style: none;
  scrollbar-width: none;
  padding: 20px;
  margin: -16px;
}
.card-wrapper::-webkit-scrollbar {
    display: none;
  }
.card-wrapper .card {
  flex-shrink: 0;
  margin-right: 1rem;
  margin-top: 2px;
}
</style>
