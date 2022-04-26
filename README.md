# **Daftar Komponen**:
1. [Card](#1-Card)
2. [CardWrapper](#2-CardWrapper)
3. [ButtonGroup](#3-ButtonGroup)
4. [Navbar](#4-Navbar)
5. [RewardBar](#5-RewardBar)

# 1. Card

## Props
- title : String
- contentType (opsional) : String
- duration (opsional) : String
- variant : String
- color : String
- newContent (opsional) : Boolean
- presenter (opsional) : String
- presenter_url : String
- disabled (opsional) : Boolean
- href : String

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
- items : Array
- disabled : Boolean (opsional)

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
- page : String
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
- point : String
- streak : String
- key_point : String
- setting : Boolean
- back : Boolean
- light : Boolean
## Contoh Penggunaan
### 1. RewardBar normal
![Contoh RewardBar](https://cdn.discordapp.com/attachments/390287367128481792/968421511675396116/reward-bar.png)
```
<template>
  <header>
    <RewardBar :point="9999" :streak="99" :key_point="99"></RewardBar>
  </header>
</template>
```
### 2. RewardBar light
![Contoh RewardBar Light](https://cdn.discordapp.com/attachments/390287367128481792/968421509846675476/reward-bar-light.png)
```
<template>
  <header>
    <RewardBar point="6" streak="01" key_point="03" :setting="false" back light></RewardBar>
  </header>
</template>
```
