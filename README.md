# **Kuncie UI Engineer Test**
### Project Setup
```sh
npm install
```
### Compile and Hot-Reload for Development
```sh
npm run dev
```

# Daftar Komponen:
1. [Card](#1-Card)
2. [CardWrapper](#2-CardWrapper)
3. [ButtonGroup](#3-ButtonGroup)
4. [Navbar](#4-Navbar)
5. [RewardBar](#5-RewardBar)

# 1. Card

## Props

Contoh penggunaan props dan hasil pada elementnya dapat dilihat di bawah bagian ini.
- **title (String)**         : Teks judul dalam card
- **contentType (String)**   : Teks kecil untuk jenis variant "video", **opsional**.
- **duration (String)**      : Teks kecil untuk deskripsi durasi pada variant card "video", **opsional**. 
- **variant (String)**       : Dapat diisi dengan "video" atau "module". Mengubah jenis Card yang ditampilkan.
- **color (String)**         : Dapat diisi dengan "blue", "yellow", atau "red". Mengubah warna background Card.
- **newContent (Boolean)**   : Memberikan tag "Baru" pada pojok kiri atas Card, **opsional**.
- **presenter (String)**     : Teks nama pemateri yang akan ditampilkan pada Card.
- **presenter_url (String)** : Link untuk foto pemateri yang akan ditampilkan pada Card.
- **disabled (Boolean)**     : Mengubah Card menjadi abu-abu/disabled.
- **href (String)**          : Link yang dituju jika mengeklik Card.

## Penjelasan props menggunakan gambar
![Card Explanation 3](https://cdn.discordapp.com/attachments/390287367128481792/968422375718789130/Group_6.png)
![Card Explanation 2](https://cdn.discordapp.com/attachments/390287367128481792/968422375949484122/Group_5.png)
![Card Explanation 1](https://cdn.discordapp.com/attachments/390287367128481792/968421490691276800/explanation-1.jpg)
## Contoh Penggunaan

### - Card video berwarna biru

![Contoh Card Video Biru](https://cdn.discordapp.com/attachments/390287367128481792/968421510089936946/video-blue.png)
```
<Card
  title="Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran"
  variant="video"
  duration="2:30 min"
  color="blue"
  contentType="Video"
  presenter_url="src/assets/png/presenter-1.png"
  href="/module.html"
/>

```
### - Card module berwarna merah
![Contoh Card Module Merah](https://cdn.discordapp.com/attachments/390287367128481792/968421510895263764/module-red.jpg)

```
<Card
  title="Kiat-kiat Menjadi Penulis Kreatif ala Raditya Dika"
  variant="module"
  color="red"
  presenter="Raditya Dika"
  presenter_url="src/assets/png/presenter-3.png"
  href="/module.html"
/>
```
### - Card module berwarna merah dengan tag baru
![Contoh Card Module Baru Kuning](https://cdn.discordapp.com/attachments/390287367128481792/968421511465697290/new-yellow.jpg)
```
<Card
  title="Kiat-kiat Menjadi Penulis Kreatif ala Raditya Dika"
  variant="module"
  color="yellow"
  presenter="Raditya Dika"
  presenter_url="src/assets/png/presenter-1.png"
  href="/module.html"
  :newContent="true"
/>
```
### - Card Video dengan prop disabled
![Contoh Card Disabled](https://cdn.discordapp.com/attachments/390287367128481792/968421510605860884/disabled.png)
```
<Card
  title="Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran"
  variant="video"
  duration="2:30 min"
  contentType="Video"
  presenter_url="src/assets/png/presenter-1.png"
  href="/module.html"
  disabled
/>
```
# 2. CardWrapper

## Props
- **items (Array)** : Array Object berisikan props untuk tiap Card yang dirender.
- **disabled (Boolean)** : Mengubah semua Card di dalam wrapper menjadi disabled.

![Contoh CardWrapper](https://cdn.discordapp.com/attachments/390287367128481792/968424328838393896/unknown.png)
## Contoh Penggunaan
```
<script>
import CardWrapper from "./components/CardWrapper.vue";

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
]
</script>

<template>
  <main>
    <CardWrapper :items="exampleVidList"></CardWrapper>
  </main>
</template>
```

# 3. ButtonGroup
## Contoh Penggunaan
![Contoh Button Group](https://cdn.discordapp.com/attachments/390287367128481792/968421510333222972/button-group.png)
```
<template>
  <ButtonGroup>
    <button class="active">Konten</button>
    <button>Materi</button>
  </ButtonGroup>
</template>
```

# 4. Navbar
## Props
- **page (String)** : Dapat diisi dengan "home", "people", "message", atau "history". Menandakan tombol mana yang berstatus aktif.
## Contoh Penggunaan
![Contoh Navbar](https://cdn.discordapp.com/attachments/390287367128481792/968421511226609725/navbar.png)
```
<template>
  <main>
    <Navbar page="home"></Navbar>
  </main>
</template>
```

# 5. RewardBar
## Props
- **point (String)** : Teks yang menandakan jumlah point yang dimiliki.
- **streak (String)** : Teks yang menandakan jumlah streak yang dimiliki.
- **key_point (String)** : Teks yang menandakan jumlah key yang dimiliki.
- **setting (Boolean)** : Menampilkan tombol setting di ujung kanan. Default: True.
- **back (Boolean)** : Menampilkan tombol back di ujung kiri. Default: False.
- **light (Boolean)** : Mengubah RewardBar menjadi bertema terang jika bernilai True.
## Contoh Penggunaan
### 1. RewardBar normal + Settings Button
![Contoh RewardBar](https://cdn.discordapp.com/attachments/390287367128481792/968421511675396116/reward-bar.png)
```
<template>
  <header>
    <RewardBar :point="9999" :streak="99" :key_point="99"></RewardBar>
  </header>
</template>
```
### 2. RewardBar light + Back Button
![Contoh RewardBar Light](https://cdn.discordapp.com/attachments/390287367128481792/968421509846675476/reward-bar-light.png)
```
<template>
  <header>
    <RewardBar point="6" streak="01" key_point="03" :setting="false" back light></RewardBar>
  </header>
</template>
```
