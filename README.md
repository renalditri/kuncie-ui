# **Daftar Komponen**:
- Card
- CardWrapper
- ButtonGroup
- Navbar
- RewardBar

## Card

### Props
- title
- contentType
- duration
- variant
- color
- newContent
- presenter
- presenter_url
- disabled
- href

### Contoh Penggunaan
- Card video berwarna biru
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
- Card module berwarna merah
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
- Card module berwarna merah dengan tag baru
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
