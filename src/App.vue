<script setup>
import Card from "./components/Card.vue";
import CardWrapper from "./components/CardWrapper.vue";
import Navbar from "./components/Navbar.vue";
import RewardBar from "./components/RewardBar.vue";

const exampleVidList = [
  {
    title: "Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran",
    variant: "video",
    color: "blue",
    contentType: "Video",
    duration: "2:30 min",
    presenter_url: "src/assets/png/presenter-1.png",
    href: "module.html"
  },
  {
    title: "Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran",
    variant: "video",
    color: "red",
    contentType: "Video",
    duration: "2:30 min",
    presenter_url: "src/assets/png/presenter-2.png",
    href: "module.html"
  },
  {
    title: "Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran",
    variant: "video",
    color: "yellow",
    contentType: "Video",
    duration: "2:30 min",
    presenter_url: "src/assets/png/presenter-3.png",
    href: "module.html"
  },
];
const exampleModList = [
  {
    title: "Menjelajahi Arti Sebagai Seorang Pemimpin Muda",
    variant: "module",
    color: "blue",
    presenter: "Putri Tanjung",
    presenter_url: "src/assets/png/presenter-2.png",
    href: "module.html"
  },
  {
    title: "Kiat-kiat Menjadi Penulis Kreatif ala Raditya Dika",
    variant: "module",
    color: "yellow",
    presenter: "Raditya Dika",
    presenter_url: "src/assets/png/presenter-1.png",
    href: "module.html"
  },
  {
    title: "Kiat-kiat Menjadi Penulis Kreatif ala Raditya Dika",
    variant: "module",
    color: "red",
    presenter: "Raditya Dika",
    presenter_url: "src/assets/png/presenter-3.png",
    href: "module.html"
  },
];
const exampleModNewList = [
  {
    title: "Menjelajahi Arti Sebagai Seorang Pemimpin Muda",
    variant: "module",
    color: "blue",
    presenter: "Putri Tanjung",
    presenter_url: "src/assets/png/presenter-2.png",
    newContent: true,
    href: "module.html"
  },
  {
    title: "Kiat-kiat Menjadi Penulis Kreatif ala Raditya Dika",
    variant: "module",
    color: "yellow",
    presenter: "Raditya Dika",
    presenter_url: "src/assets/png/presenter-1.png",
    newContent: true,
    href: "module.html"
  },
  {
    title: "Kiat-kiat Menjadi Penulis Kreatif ala Raditya Dika",
    variant: "module",
    color: "red",
    presenter: "Raditya Dika",
    presenter_url: "src/assets/png/presenter-3.png",
    newContent: true,
    href: "module.html"
  },
];
</script>

<template>
  <header>
    <RewardBar :point="9999" :streak="99" :key_point="99"></RewardBar>
    <h1>Hai Kuncoro!</h1>
    <br />
    <input
      class="search-bar body-1"
      type="text"
      placeholder="Cari Topik, Konten, atau Mentor"
    />
  </header>
  <main>
    <section class="section-1">
      <div class="heading">
        <h2>Rencana Belajar</h2>
        <span class="body-2">Lihat Rencana</span>
      </div>
      <CardWrapper :items="exampleVidList"></CardWrapper>
    </section>
    <section class="section-2">
      <h2>Lagi Trending 📈</h2>
      <CardWrapper :items="exampleModList"></CardWrapper>
      <h2 style="margin-top: 1rem">Unboxing modul barunya, yuk!</h2>
      <CardWrapper :items="exampleModNewList"></CardWrapper>
    </section>
  </main>
  <Navbar page="home"></Navbar>
</template>

<style>
@import "./assets/base.css";
main {
  padding-bottom: 4.25rem;
}
#app {
  width: 360px;
  margin: 0 auto;
  background-color: #2c1a32;
  font-weight: normal;
}
header h1 {
  margin-bottom: 1rem;
}

section h2 {
  margin-bottom: 1rem;
}

.section-1 {
  margin: 1rem;
}

.section-1 h2 {
  display: inline-block
}

.section-1 .heading{
  display: flex;
  justify-content: space-between;
  align-items: baseline;
}

.section-2 {
  background: #ffffff;
  border-radius: 20px 20px 0px 0px;
  padding: 1.5rem 1rem;
  margin: 0px;
}

.section-2 h2 {
  color: black;
}

.search-bar {
  background: #413147;
  border-radius: 40px;
  width: 100%;
  padding: 0.75rem 1rem;
  border: none;
}

@media (min-width: 1024px) {
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
    padding: 1rem 1rem 1rem 1rem;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  .logo {
    margin: 0 2rem 0 0;
  }
}
</style>
