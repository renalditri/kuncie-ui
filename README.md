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

![asd](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/explanation-3.png?token=GHSAT0AAAAAABRZJKXROFWGN2AZ5CAMPSV2YTGXN4A)
![asd](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/explanation-2.png?token=GHSAT0AAAAAABRZJKXQGONUBKUNOGRQQ7T2YTGXNNA)
![asd](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/explanation-1.jpg?token=GHSAT0AAAAAABRZJKXQURYEFVJ22SIT3B3KYTGXMKA)
## Contoh Penggunaan

### - Card video berwarna biru

![Contoh Card Video Biru](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/video-blue.png?token=GHSAT0AAAAAABRZJKXRMQM2LVM4FJU4MN76YTGXWFA)
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
![Contoh Card Module Merah](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/module-red.jpg?token=GHSAT0AAAAAABRZJKXR3LPLLXSPJXWGM35AYTGXY2A)

```
<Card
  title="Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran"
  variant="module"
  color="blue"
  presenter="Putri Tanjung"
  presenter_url="src/assets/png/presenter-1.png"
  href="/module.html"
/>
```
### - Card module berwarna merah dengan tag baru
![Contoh Card Module Baru Kuning](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/new-yellow.jpg?token=GHSAT0AAAAAABRZJKXRGKRR3VPNV7RFBPMUYTGXY4A)
```
<Card
  title="Menulis Kreatif dan Terstruktur agar Produk Laris di Pasaran"
  variant="module"
  color="blue"
  presenter="Putri Tanjung"
  presenter_url="src/assets/png/presenter-1.png"
  href="/module.html"
  :newContent="true"
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
![Contoh Button Group](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/button-group.png?token=GHSAT0AAAAAABRZJKXQXUUVATCFDA3QJXC6YTGYDOQ)
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
![Contoh Navbar](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/navbar.png?token=GHSAT0AAAAAABRZJKXQPAA3UZRILSSQZA7SYTGYFCA)
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
![Contoh RewardBar](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/reward-bar.png?token=GHSAT0AAAAAABRZJKXRKPNJMDLXUB7O3J72YTGYIQA)
```
<template>
  <header>
    <RewardBar :point="9999" :streak="99" :key_point="99"></RewardBar>
  </header>
</template>
```
### 2. RewardBar normal
![Contoh RewardBar](https://raw.githubusercontent.com/renalditri/kuncie-ui/main/tutorial/reward-bar-light.png?token=GHSAT0AAAAAABRZJKXR7SL4PD3UJFKPNQV2YTGYH2A)
```
<template>
  <header>
    <RewardBar point="6" streak="01" key_point="03" :setting="false" back light></RewardBar>
  </header>
</template>
```
