# DESAIN SISTEM — berita.mountaineering-indonesia.org

> Dokumen ini adalah hasil reverse engineering dari `index.html` master.
> Semua komponen baru WAJIB mengikuti spesifikasi di sini — tidak boleh mengarang sendiri.
> Diperbarui: Juni 2026

---

## 1. Token Warna

```css
--red:        #C8102E   /* aksen utama: CTA, border, tag FMI, hover */
--black:      #111111   /* background gelap, teks utama, tag eksternal */
--white:      #FFFFFF   /* background halaman */
--white-off:  #F8F7F5   /* hover card, background caption */
--gray-light: #EBEBEB   /* border card */
--gray-mid:   #888888   /* teks sekunder, tanggal, dot, footer */
--text-main:  #111111   /* judul card */
--text-sub:   #555555   /* deskripsi card, sumber */
```

---

## 2. Tipografi

| Peran | Font | CSS Variable |
|-------|------|--------------|
| Display / Judul besar | Bebas Neue | `--font-display` |
| Body / Paragraf artikel | Crimson Pro | `--font-serif` |
| UI / Label / Nav / Meta | DM Sans | `--font-body` |

Google Fonts load order:
```
Bebas+Neue&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500
```

---

## 3. Sistem Bilingual

Dua atribut data dipakai secara konsisten:

```html
<span data-id>Teks Indonesia</span>
<span data-en>English Text</span>
```

CSS toggle:
```css
[data-en] { display: none; }                      /* default: EN tersembunyi */
.lang-en [data-id] { display: none; }
.lang-en [data-en] { display: revert; }
.lang-id [data-id] { display: revert; }
.lang-id [data-en] { display: none; }
```

Aturan penerapan:
- Setiap elemen teks yang tampil ke pengguna = wajib punya pasangan `data-id` dan `data-en`
- Elemen yang TIDAK bilingual: tag kategori (uppercase Indonesia, berlaku untuk keduanya), nama sumber, angka, simbol

---

## 4. Logika Warna Tag

Tag kategori memakai inline `style="background:..."` — **bukan** class CSS.

| Warna | Kode | Kapan dipakai |
|-------|------|--------------|
| Merah | `#C8102E` | Artikel **milik FMI** — dibuat sendiri, lokal, sumber FMI |
| Hitam | `#111111` | Artikel **dari sumber eksternal** — media lain, link keluar |

Contoh:
```html
<!-- Artikel FMI sendiri -->
<span class="card-tag" style="background:#C8102E">ORGANISASI</span>

<!-- Artikel dari Kompas -->
<span class="card-tag" style="background:#111111">STANDARISASI</span>
```

---

## 5. Komponen Card

### 5A. Card dengan Thumbnail (news-card--thumb)
Dipakai untuk: artikel lokal yang punya file HTML + gambar di `img/`.

```html
<article class="news-card news-card--thumb reveal">
  <div class="card-thumb">
    <img src="img/{NNN}-{slug}.jpg" alt="{JUDUL_ID}" loading="lazy">
  </div>
  <div class="card-content">
    <div class="card-meta">
      <span class="card-tag" style="background:#C8102E">{TAG}</span>
      <span class="card-source">{SUMBER}</span>
      <span class="card-dot">·</span>
      <span class="card-date" data-id>{TANGGAL_ID}</span>
      <span class="card-date" data-en>{TANGGAL_EN}</span>
    </div>
    <h2 class="card-title">
      <span data-id>{JUDUL_ID}</span>
      <span data-en>{JUDUL_EN}</span>
    </h2>
    <p class="card-desc" data-id>{EXCERPT_ID}</p>
    <p class="card-desc" data-en>{EXCERPT_EN}</p>
    <a class="card-link" href="{NNN}-{slug}.html" target="_blank">
      <span data-id>Baca Selengkapnya</span><span data-en>Read More</span>
      <span class="link-arrow">↗</span>
    </a>
  </div>
</article>
```

### 5B. Card dengan Icon (news-card--icon)
Dipakai untuk: artikel eksternal (link ke media lain).

```html
<article class="news-card news-card--icon reveal">
  <div class="card-icon-col">
    <span class="card-icon-box">{EMOJI}</span>
  </div>
  <div class="card-content">
    <div class="card-meta">
      <span class="card-tag" style="background:#111111">{TAG}</span>
      <span class="card-source">{SUMBER}</span>
      <span class="card-dot">·</span>
      <span class="card-date" data-id>{TANGGAL_ID}</span>
      <span class="card-date" data-en>{TANGGAL_EN}</span>
    </div>
    <h2 class="card-title">
      <span data-id>{JUDUL_ID}</span>
      <span data-en>{JUDUL_EN}</span>
    </h2>
    <p class="card-desc" data-id>{EXCERPT_ID}</p>
    <p class="card-desc" data-en>{EXCERPT_EN}</p>
    <a class="card-link" href="{URL_EKSTERNAL}" target="_blank" rel="noopener">
      <span data-id>Baca Selengkapnya</span><span data-en>Read More</span>
      <span class="link-arrow">↗</span>
    </a>
  </div>
</article>
```

### Perbedaan kritis antara 5A dan 5B

| Aspek | Thumb (5A) | Icon (5B) |
|-------|-----------|-----------|
| Tag warna | `#C8102E` (merah) | `#111111` (hitam) |
| Link `href` | File lokal: `{NNN}-{slug}.html` | URL eksternal penuh |
| Link `rel` | Tidak ada | `rel="noopener"` wajib |
| Deskripsi bilingual | `<p data-id>` + `<p data-en>` terpisah | Sama |

---

## 6. Spesifikasi Elemen Card

| Elemen | Class | Font | Size | Weight | Color |
|--------|-------|------|------|--------|-------|
| Tag kategori | `.card-tag` | DM Sans | 0.62rem | 500 | white |
| Nama sumber | `.card-source` | DM Sans | 0.76rem | 500 | `--text-sub` |
| Pemisah dot | `.card-dot` | — | 0.75rem | — | `--gray-mid` |
| Tanggal | `.card-date` | DM Sans | 0.76rem | — | `--gray-mid` |
| Judul card | `.card-title` | **Bebas Neue** | clamp(1.2rem, 2vw, 1.7rem) | — | `--text-main` |
| Deskripsi | `.card-desc` | **Crimson Pro** | 1rem | — | `--text-sub` |
| Link CTA | `.card-link` | DM Sans | 0.72rem | 500 | `--red` |
| Panah link | `.link-arrow` | — | 1rem | — | inherited |

---

## 7. Emoji per Kategori Tag

| Emoji | Tag |
|-------|-----|
| ⛰️ | EKSPEDISI |
| 🛡️ | KESELAMATAN |
| 📋 | STANDARISASI |
| 🤝 | KERJASAMA |
| 🎓 | PELATIHAN |
| 📣 | ORGANISASI |
| 🌿 | LINGKUNGAN |
| 🏆 | KOMPETISI |
| 🌐 | INTERNASIONAL |

Emoji hanya dipakai pada card icon (5B). Card thumb (5A) tidak punya icon col.

---

## 8. Komponen Lain

### Nav
```
bg: black | height: 64px | border-bottom: 2px solid red
Logo: 34px height
Links: DM Sans 0.78rem fw500 letter-spacing 0.12em uppercase
Hover: color red
Lang toggle: border 1px solid rgba(255,255,255,0.2) | border-radius 2px
Button aktif: bg red, color white
```

### Page Header (index)
```
bg: black | padding: 4rem 2.5rem 3rem | border-bottom: 2px solid red
Label atas: DM Sans 0.7rem fw500 letter-spacing 0.25em uppercase color red
H1: Bebas Neue clamp(3rem, 6vw, 5rem) white line-height 1 letter-spacing 0.02em
```

### Footer
```
bg: black | padding: 1.75rem 2.5rem
flex justify-between align-center
font-size: 0.75rem letter-spacing 0.05em color gray-mid
```

### Scroll Animation
Semua card pakai class `reveal`. JavaScript IntersectionObserver menambah class `visible` saat masuk viewport, dengan delay bertahap (`i * 60ms`).

---

## 9. Gambar Thumbnail

- Ukuran kolom thumbnail: **220px** lebar
- `object-fit: cover` + `object-position: center bottom`
- Hover: `transform: scale(1.03)`
- **Orientasi gambar yang ideal: landscape atau square** — portrait akan terpotong buruk
- Format: `.jpg` | Nama: `img/{NNN}-{slug}.jpg`
- Ukuran file: max 2MB | Lebar min: 1200px

---

## 10. Responsive (max-width: 700px)

- Card thumb: `grid-template-columns: 1fr` (stack vertikal)
- Thumb height: 200px
- Nav links: `display: none`
- Padding dikurangi di semua section

---

## Catatan Penting untuk Pembuatan Konten Baru

1. **Jangan pernah buat class CSS baru** — gunakan class yang sudah ada
2. **Tag wajib pakai inline style** — bukan class
3. **Judul pakai `<h2 class="card-title">`** — bukan `<span>`
4. **Deskripsi dua elemen `<p>` terpisah** — bukan satu `<p>` dengan dua span
5. **"Baca Selengkapnya" selalu ada** — di semua card, tanpa terkecuali
6. **Class `reveal` wajib** di setiap `<article>` — untuk animasi scroll
7. **DILARANG KERAS base64 inline untuk foto artikel/card** — lihat § 11 di bawah, ini pernah merusak index.html produksi berkali-kali.

---

## 11. Larangan Base64 Inline untuk Foto (KRITIS — pernah menyebabkan outage)

**Aturan:** foto artikel dan foto card (`<img>` di `.card-thumb` maupun `.article-photo`) **WAJIB** memakai `src="img/{slug}.jpg"` yang menunjuk ke file fisik di folder `img/`. **TIDAK BOLEH** `src="data:image/...;base64,...."` inline.

**Logo FMI di `.nav-logo` juga TIDAK BOLEH base64 dan TIDAK BOLEH URL eksternal ke mountaineering-indonesia.org.** Per 1 Jul 2026, logo di-host sebagai file fisik permanen di repo ini: `berita/img/fmi-logo.jpg` (45.9KB, JPEG, 1372x644). Semua halaman (index + tiap artikel) WAJIB pakai:

```html
<img src="img/fmi-logo.jpg" alt="FMI">
```

Riwayat kenapa ini berubah:
- Awalnya template pakai `src="https://mountaineering-indonesia.org/img/fmi-logo.png"` (URL absolut ke situs utama). Situs utama beberapa kali mengganti/menghapus aset itu tanpa pemberitahuan → logo mendadak 404 di semua artikel baru. Kejadian berulang, terakhir pada artikel #047 (1 Jul 2026).
- Sebagai tambal sulam, sempat dipakai base64 inline (±61KB per file, digandakan di 38 file = total >2MB duplikasi) supaya lepas dari ketergantungan situs utama. Ini menghindari masalah 404, TAPI menciptakan risiko baru: mendekatkan ukuran file ke batas ~200-418KB yang disebut di atas (lihat insiden dasar masalah ini).
- Solusi permanen (per 1 Jul 2026): logo di-host sendiri sebagai file relatif di `berita/img/fmi-logo.jpg`, sama seperti foto artikel biasa. Tidak tergantung situs eksternal, tidak membengkakkan file HTML.

**Kalau butuh ganti logo di masa depan:** update satu file `berita/img/fmi-logo.jpg` saja — otomatis berlaku ke semua halaman lama & baru karena semuanya rujuk ke path relatif yang sama. Jangan pernah kembali ke base64 atau URL absolut situs utama untuk elemen ini.

**Kenapa ini kritis:** sandbox bash yang dipakai untuk deploy (Cloudflare + GitHub) punya batas baca keras di sekitar ~418KB per file. Kalau sebuah file HTML (terutama `index.html`, yang isinya numpuk puluhan card) melewati batas itu karena ada foto yang di-embed base64 la