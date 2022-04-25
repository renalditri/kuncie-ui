<script setup>
import Card from "./Card.vue";
const props = defineProps({
  page: {
    type: String,
    required: true,
    default: "home",
    validators: (value) =>
      ["home", "people", "message", "history"].includes(value),
  },
});

const inPage = (page) => {
  return props.page == page ? true : false;
};

console.log(inPage("home"));
</script>

<template>
  <nav class="navbar">
    <ul class="icon-wrapper">
      <li>
        <a class="nav-icon home" :class="{ active: inPage('home') }"> </a>
      </li>
      <li>
        <a class="nav-icon people" :class="{ active: inPage('people') }"> </a>
      </li>
      <li>
        <a class="nav-icon message" :class="{ active: inPage('message') }"> </a>
      </li>
      <li>
        <a class="nav-icon history" :class="{ active: inPage('history') }"> </a>
      </li>
      <li class="menu-icon">
        <img class="menu-icon" src="../assets/svg/icons/menu.svg" />
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  width: 360px;
  position: fixed;
  bottom: 0;
  margin: auto;
  background-color: white;
  padding: 1rem;
  box-shadow: 0px -2px 4px rgba(0, 0, 0, 0.05);
}
.icon-wrapper {
  list-style-type: none;
  position: relative;
  padding: 0rem;
}
.navbar li {
  display: inline-block;
}
.nav-icon {
  display: inline-block;
  width: 24px;
  height: 24px;
  background-color: #cccccc;
  margin: 3px 1.125rem;
}
.nav-icon:hover {
  background-color: #535353;
}
.menu-icon {
  position: absolute;
  bottom: 0rem; 
  right: 0rem;
}
.active {
  background-color: black;
}

.nav-icon.home {
  mask-image: url("../assets/svg/icons/home.svg");
}

.nav-icon.people {
  mask-image: url("../assets/svg/icons/users.svg");
}
.nav-icon.message {
  mask-image: url("../assets/svg/icons/message-circle.svg");
}
.nav-icon.history {
  mask-image: url("../assets/svg/icons/history.svg");
}
</style>
