<script setup>
const props = defineProps({
});
</script>

<template>
  <div class="button-group">
    <slot></slot>
  </div>
</template>

<style>
.button-group {
  background-color: #eeeef1;
  border-radius: 30px;
  padding: 0px;
}

.button-group button {
  border-radius: 30px;
  background: #eeeef1;
  color: #2c1a32;
  padding: 7px 12px;
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 18px;
  text-align: center;
	border: none;
}

.button-group .active {
  border-radius: 30px;
  background: #2c1a32;
  color: #ffffff;
}
</style>
