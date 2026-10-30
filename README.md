# Coffee Bike

Website kedai kopi dan kudapan *vintage editorial* untuk Coffee Bike, Petamburan, Jakarta Barat. Dibangun murni menggunakan HTML5, CSS3, dan vanilla JavaScript tanpa dependensi build tools.

## Pratinjau Lokal

Buka langsung file `index.html` di peramban (browser) apa pun atau jalankan server lokal statis. Tidak memerlukan langkah kompilasi atau paket npm.

## Struktur Berkas & Aset

- `index.html` — Konten halaman, semantik aksesibilitas, video hero Safari-resilient, dan interaksi navigasi scroll responsif (versi CSS cache-busting `?v=2.2`).
- `theme.css` — Sistem desain vintage editorial, typography fluid, safe mobile positioning, animasi performan, dan penanganan viewport anti-overflow (`overflow-x: clip`).
- `variables.css` — Token desain: palet warna (kertas vintage, terracotta, espresso, corten), tipografi, dan dimensi layout.
- `CNAME` — Konfigurasi domain khusus.
- `Aset/optimized/` — Berkas media dan dokumentasi fotografi kedai:
  - `Header/header coffee.mp4` — Video hero suasana seduhan kopi.
  - `IMG_2723.webp` — Poster video hero dan foto polaroid *Americano Original*.
  - `Menu/1.png` — Sajian *Americano Original*.
  - `Menu/2.png` — Sajian *Kentang Donat* Little Jogja.
  - `Menu/3.png` — Sajian *Nasi & Lauk* Little Jogja.
  - `Menu/4.png` — Sajian *Es Kopi Susu*.
  - `IMG_2726.webp`, `IMG_2727.webp`, `IMG_2728.webp` — Aset sumber fotografi kedai (dipertahankan sebagai arsip sumber).
  - `americano-original.webp`, `kentang-donat.webp`, `kopi-susu.webp`, `nasi-lauk-little-jogja.webp` — Aset fotografi alternatif WebP.

## Fitur & Kompatibilitas Mobile / Tablet

1. **Anti-Overflow & Viewport Clean:**
   - Teruji pada resolusi 320px, 360px, 390px, 430px, dan 768px: `document.documentElement.scrollWidth <= clientWidth` dengan 0 elemen melebar ke samping.
2. **Navigasi Kapsul & Menu Responsif:**
   - Desktop & Tablet: Logo di kiri tanpa ikon bintang, menu links, dan tombol kunjungan berbentuk kapsul (*pill*).
   - Layar Ponsel Sempit: Fallback menu bar rapi dengan tombol aksi *Kunjungi* dan toggle drawer berlatar solid (`#FBF8F3`) tanpa tembus pandang ke teks halaman di belakangnya.
3. **Smart Scroll Interaction:**
   - Navigasi bertransisi hilang saat pengguna menggulir ke bawah (*scroll down* > 8px).
   - Navigasi muncul kembali secara halus saat menggulir ke atas (*scroll up*).
   - Navigasi tetap terkunci terlihat di posisi paling atas layar (`scrollY <= 20px`) dan saat drawer menu sedang terbuka.
4. **Media & Animasi:**
   - Video hero dengan dukungan atribut lengkap Safari/iOS (`muted`, `playsinline`, `webkit-playsinline`, `autoplay`, `loop`).
   - Animasi polaroid dengan keyframes terakselerasi perangkat keras (`-webkit-transform`, `will-change`).
   - Penuh rasa hormat terhadap preferensi pengguna `@media (prefers-reduced-motion: reduce)`.
