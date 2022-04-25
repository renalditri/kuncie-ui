# **Daftar Komponen**:
1. [Card](#1-Card)
2. CardWrapper
3. ButtonGroup
4. Navbar
5. RewardBar

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
