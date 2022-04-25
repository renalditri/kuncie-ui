<script setup>
import ButtonGroup from "./components/ButtonGroup.vue";
import RewardBar from "./components/RewardBar.vue";
import CardWrapper from "./components/CardWrapper.vue";
const exampleVidList = [
  {
    title: "Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran",
    variant: "video",
    color: "blue",
    contentType: "Video",
    duration: "2:30 min",
    presenter_url: "src/assets/png/presenter-1.png",
  },
  {
    title: "Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran",
    variant: "video",
    color: "red",
    contentType: "Video",
    duration: "2:30 min",
    presenter_url: "src/assets/png/presenter-2.png",
  },
];
</script>

<template>
  <header>
    <RewardBar point="6" streak="01" key_point="03" :setting="false" back light></RewardBar>
    <h1>Pentingnya Creative Thinking di Era Digital</h1>
    <br />
    <img class="presenter-img" src="./assets/png/presenter-1.png" />
    <ButtonGroup>
      <button class="active">Konten</button>
      <button>Materi</button>
    </ButtonGroup>
  </header>
  <main>
    <section class="section-1">
      <h3 class="section-heading">Mengenai Creative Thinking</h3>
      <p class="subtitle-2">0 dari 5 video selesai ditonton</p>
      <CardWrapper :items="exampleVidList"></CardWrapper>
    </section>
    <section class="section-2">
      <h3 class="section-heading">Penerapan Creative Thinking</h3>
      <p class="subtitle-2">Buka dengan selesaikan semua video diatas</p>
      <CardWrapper :items="exampleVidList" disabled></CardWrapper>
    </section>
  </main>
</template>

<style>
@import "./assets/base.css";
body {
  background-color: #E5E5E5;
}
.presenter-img{
  margin-top: 1rem;
  margin-bottom: 2rem;
}
#app {
  width: 360px;
  margin: 0 auto;
  background-color: #FFFFFF;
  font-weight: normal;
}
h1, .section-heading, .subtitle-2 {
  color: #09050A;
}
.reward-bar {
  display: flex;
  margin-top: -4px;
  margin-bottom: 1rem;
}
body {
  display: flex;
  place-items: center;
}

#app {
  display: flex;
  flex-direction: column;
}

header {
  display: flex;
  flex-direction: column;
  align-items: start;
  padding: 1rem 1rem 0rem 1rem;
}
header .wrapper {
  display: flex;
  place-items: flex-start;
  flex-wrap: wrap;
}
.presenter-img {
  border-radius: 1000px;
  width: 48px;
  height: 48px;
}

.section-1 {
  margin: 1rem;
}
.section-2 {
  margin: 1rem;
}
</style>
