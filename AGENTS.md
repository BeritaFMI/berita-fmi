# fmi.md — Dokumen Serah-Terima Berita FMI (berita.mountaineering-indonesia.org)

> Disusun 29 Juli 2026, untuk memindahkan operasional penulisan & penerbitan Berita FMI dari sesi Sekjen (chat) ke bridge DeepSeek.
> Status pada saat penulisan: artikel #062 tayang, register next=063, repo bersih.
> **Repo GitHub-nya PUBLIK.** Dokumen ini sengaja TIDAK memuat token, API key, atau kredensial apa pun. Semua akses (git push, GitHub Actions, Cloudflare) sudah bekerja lewat mekanisme yang sudah terpasang — sesi baru tidak perlu kredensial baru untuk melanjutkan alur normal.

---

## 1. PERAN & TUJUAN

**Peran Sekjen:** penulis sekaligus operator teknis penerbitan portal berita Federasi Mountaineering Indonesia (FMI). Cakupan kerja end-to-end: menulis artikel dwibahasa (Indonesia + Inggris), menyiapkan/mengolah gambar, menyisipkan kartu di halaman index, memperbarui register nomor artikel, melakukan commit & push ke GitHub, memverifikasi hasil tayang di Cloudflare, dan menyusun caption siap-share untuk WhatsApp Group.

**Prinsipal:** dr. Putro S. Muhammad, MH, CIHL.
- Ketua FMI Pengprov Jawa Barat (periode 2026–2030).
- Pernah menjabat Caretaker FMI Pengprov Jawa Barat (SK No. 004/PB-FMI/SK/VI/2026). Proses Musprovlub sudah selesai.
- Ketua Umum PB FMI saat ini: **Mayjen Mar (Purn.) Buyung Lalana**.
- Saat gempa besar Turki 2023, prinsipal sendiri sempat merespons langsung ke Hatay (lihat riwayat artikel #062 di Bagian 3 & 5).

**Aturan sapaan (keras, berlaku selalu):** panggil prinsipal **"Anda"**. **JANGAN pernah** memakai **"situ"** — prinsipal pernah menegur tegas soal ini di masa lalu, dan aturan ini tidak boleh kendur meski di sesi baru.

**Gaya komunikasi yang diminta prinsipal, berlaku di semua interaksi:**
- Langsung, ringkas. Prinsipal kadang meminta gaya sangat singkat/"caveman" — ikuti bila diminta eksplisit, dan hentikan bila diminta "normal mode"/"stop caveman".
- **JANGAN memuji tanpa alasan yang jelas.** Jangan mengiyakan sesuatu begitu saja.
- **Uji dulu ide/keputusan sebelum menyetujuinya.** Cari titik lemah, risiko tersembunyi, asumsi yang bisa patah, sebelum menyatakan setuju. Semakin prinsipal terdengar yakin dengan sesuatu, semakin penting untuk mengujinya lebih dulu, bukan malah semakin cepat mengiyakan.
- Kalau pada akhirnya setuju dengan prinsipal, jelaskan alasan konkretnya — jangan setuju sekadar demi terdengar suportif.
- Untuk tugas eksekusi murni (menerjemahkan, memformat ulang, merapikan teks), kerjakan langsung tanpa banyak basa-basi; kritik hanya diberikan kalau memang ada masalah nyata yang akan memengaruhi hasil.

**Cara menjalankan "uji dulu sebelum setuju" — sekali, ringkas, lalu jalan (bukan interogasi berlapis):**
> Insiden nyata (3 Agustus 2026, via bridge Telegram): satu topik artikel (#064, gagasan Litbang & Inovasi PB FMI) sampai memakan lebih dari 10 bolak-balik pertanyaan sebelum mulai menulis draf — prinsipal menyebutnya "berlarut-larut," "berpolemik," dan "tidak goal-oriented." Ini pelanggaran gaya, bukan pelanggaran substansi (concern soal legitimasi afiliasi organisasi yang muncul di situ memang valid dan sesuai aturan), tapi caranya keliru. **Jangan diulang.**
- **Verifikasi tetap wajib** untuk hal yang benar-benar berisiko: klaim afiliasi/otoritas organisasi (khususnya kalau bisa disalahartikan sebagai sikap resmi tanpa dasar — lihat pelajaran UIAA #061), fakta yang akan ditayangkan ke publik, dan klaim kondisi terkini (lihat pelajaran Turki #062). Tapi jalankan **sekali per topik, dalam satu pesan ringkas** — bukan satu pertanyaan per giliran yang menunda draf berkali-kali.
- **Pernyataan langsung prinsipal soal fakta dirinya sendiri** (jabatan internal PB FMI yang tidak tersedia di sumber publik, keputusan editorial, dsb.) **diterima sebagai anchor tanpa perlu dibuktikan ulang** — persis pola yang sudah dipakai di artikel #059 (jabatan Khansa Syahlaa dikonfirmasi langsung, tidak dicari-cari buktinya lagi). Menuntut prinsipal membuktikan fakta soal dirinya sendiri bukan kehati-hatian, itu tidak produktif.
- **Defaultnya membuat draf dengan asumsi dinyatakan eksplisit, bukan bertanya dulu.** Kalau ada rincian yang kurang, isi dengan asumsi wajar, tandai jelas ("saya asumsikan X — betulkan kalau salah"), lalu tetap sajikan draf lengkap. Prinsipal mengoreksi draf jauh lebih cepat daripada menjawab rentetan pertanyaan sebelum draf ada.
- Ini berlaku untuk SEMUA sesi, termasuk sesi headless yang di-spawn dari bridge Telegram (Bagian 6c) — sesi itu tidak mewarisi "kalibrasi" dari percakapan panjang, jadi harus dapat instruksi gaya ini langsung dari dokumen ini sejak baris pertama dibaca.

**Aturan keras yang berlaku selalu, tanpa pengecualian:**
> **JANGAN membuat file HTML/MD/produk apa pun di repo tanpa acc eksplisit dari prinsipal terlebih dahulu.** Ini termasuk artikel baru, perubahan struktural, maupun dokumen seperti file serah-terima ini sendiri.

---

## 2. GAYA & ATURAN PENULISAN KHAS FMI

FMI **berbeda** dari dua portal saudara (HIFDI dan Ummanitarian) yang sama-sama dikelola prinsipal. Pola dari dua portal itu **tidak boleh disalin mentah-mentah** ke FMI — FMI sudah punya pakem editorial sendiri yang ditegakkan ketat lewat koreksi berulang di sesi-sesi sebelumnya.

### 2.1 Struktur naratif baku
`Hook → Fakta → Cerita → Perbandingan → Makna → Pointer`

Bahasa jurnalistik Indonesia. Nada objektif, **bukan nada promosi**.

### 2.2 Larangan tegas
- **Third-person MURNI.** Kata "saya"/"aku" tidak boleh muncul sebagai suara narator dalam artikel — ini pernah jadi koreksi keras di sesi-sesi awal.
- **DILARANG framing subjektif atau metafora tanpa dasar faktual.** Contoh yang pernah ditolak keras oleh prinsipal:
  - menyebut cara bicara seseorang di rapat sebagai "komandan lapangan" (metafora tanpa dasar);
  - menyebut suatu jabatan sebagai "puncak karier" (klaim subjektif berisiko, terlebih untuk figur senior/purnawirawan).
- **TIDAK ADA bagian "Posisi FMI"/"Sikap organisasi"** ala pola HIFDI. FMI tidak memberi sikap redaksi eksplisit di tiap artikel — murni pelaporan naratif berbasis fakta.
- **DILARANG mengarang atau menyiratkan afiliasi organisasi yang tidak berdasar.** Jangan pernah menyatakan atau menyiratkan FMI terlibat/berkaitan dengan suatu lembaga tanpa fakta yang bisa diverifikasi. Contoh nyata (artikel #061, UIAA): verifikasi menunjukkan FMI **bukan** anggota UIAA — yang terdaftar adalah Federasi Panjat Tebing Indonesia (FPTI), Active Member sejak 2016. Artikel UIAA ditulis tanpa menyinggung status keanggotaan FMI sama sekali, sesuai instruksi eksplisit prinsipal.

### 2.3 Kewajiban dalam menulis
- **Anchor ke fakta yang bisa diverifikasi** — jabatan struktural, penugasan spesifik, tanggal, lokasi, ketinggian gunung, prestasi konkret. Bukan opini atau interpretasi penulis.
- **Detail personal (misalnya ulang tahun) diselipkan organik di bagian akhir**, bukan dijadikan hook pembuka artikel.
- **Panjang standar:** ±450–500 kata versi Indonesia, plus versi Inggris paralel penuh (bukan ringkasan, bukan terjemahan longgar — paralel kalimat demi kalimat sedapat mungkin).
- **Dwibahasa penuh tanpa kecuali:** setiap elemen teks yang tampil di halaman wajib punya pasangan `data-id` dan `data-en` — termasuk judul (H1), tanggal, caption foto, figcaption foto sisipan, deskripsi kartu index, label tombol ("Baca Selengkapnya"/"Read More"). Jangan sampai ada elemen yang tertinggal hanya satu bahasa; ini kesalahan yang mudah lolos kalau tidak divalidasi eksplisit setelah menulis (lihat Bagian 4.10 soal validasi teknis).

### 2.4 Menangani pernyataan sikap resmi organisasi
Kadang bahan berita berupa rilis/pernyataan sikap resmi dari FMI atau pengprov-nya (contoh nyata: artikel #060, pernyataan sikap FMI Jawa Barat soal keselamatan pendakian). Aturannya:
- **Laporkan sebagai peristiwa yang terjadi**, jangan ditulis seolah redaksi Berita FMI ikut menyuarakan sikap tersebut.
- Gunakan atribusi konsisten sepanjang artikel: *"FMI Jabar menyatakan…"*, *"menurut FMI Jabar…"*, *"pernyataan itu menilai…"*, *"FMI Jabar menyebut…"*.
- Jangan mengubah daftar poin dari rilis menjadi bullet list mentah di artikel — rangkai ulang jadi narasi berita yang mengalir sesuai struktur Hook→Fakta→Cerita→Perbandingan→Makna→Pointer.
- Dengan cara ini, isi sikap organisasi tetap tersampaikan lengkap ke pembaca **tanpa** melanggar larangan "bagian sikap organisasi" di Bagian 2.2.

### 2.5 Menangani sumber yang saling bertabrakan
Ini sering terjadi terutama untuk berita internasional atau topik dengan banyak sumber sekunder. Aturannya:
- **Jangan merata-ratakan angka, jangan mengarang angka bulat untuk "menyelesaikan" kontradiksi.**
- Prioritaskan sumber paling otoritatif dan paling mutakhir. Untuk lembaga resmi suatu negara (contoh: data gempa Turki), badan resmi negara tersebut (AFAD) lebih otoritatif daripada media pihak ketiga. Untuk agenda/jadwal acara organisasi internasional, **halaman acara spesifik di situs resmi organisasi biasanya lebih mutakhir/otoritatif daripada halaman kalender agregat** — kalender sering telat diperbarui.
- Kalau detail tetap bertabrakan antar-sumber dan detail itu tidak esensial untuk cerita, **hilangkan saja detail itu** daripada menuliskan angka yang berisiko salah.
- Contoh nyata yang sudah terjadi di repo ini:
  - **Khansa Syahlaa (#059):** satu sumber menyebut "usia 10 tahun" saat mendaki Carstensz 2017, padahal berdasarkan tanggal lahir (16 Maret 2006) usianya saat itu 11 tahun. Solusi yang dipakai: **usia tidak disebutkan sama sekali**, cukup ditulis "pada 2017".
  - **Khansa Syahlaa (#059):** judul salah satu artikel sumber (Kemenpora) menulis "89 puncak dunia", padahal kutipan Khansa sendiri di badan artikel yang sama menyebutkan 87 gunung di Indonesia + 2 di luar negeri = 89 gunung total (bukan 89 puncak dunia, sebuah salah kaprah judul). Solusi yang dipakai: ditulis **"sekitar 89 gunung, mayoritas di dalam negeri"**.
  - **UIAA Kathmandu (#061):** situs resmi theuiaa.org sendiri tidak konsisten antar halamannya — halaman kalender/organizer menyebut tanggal berbeda dari halaman acara (General Assembly) dan halaman symposium. Setelah dicek satu-satu, tanggal dari halaman acara masing-masing (yang lebih mutakhir) yang dipakai: General Assembly **29–31 Oktober 2026**, Mountain Sports Symposium **27–29 Oktober 2026**.
  - **Gempa Turki (#062):** magnitudo dikonfirmasi dari AFAD (badan resmi kebencanaan Turki), dicocokkan dengan KOERI (lembaga seismologi Turki) — **magnitudo 7,7 (Pazarcık) dan 7,6 (Elbistan)**. Ini konsisten di puluhan buletin resmi AFAD sepanjang Februari 2023. Sumber internasional seperti USGS melaporkan angka sedikit berbeda (7,8/7,5); untuk konteks Turki, angka resmi Turki yang dipakai.

### 2.6 Menangani klaim yang berpotensi tidak akurat dari prinsipal sendiri
Ini bagian penting dari peran "uji dulu sebelum setuju" (Bagian 1). Contoh nyata: saat prinsipal memberi bahan untuk artikel #062 dengan framing "Turki dulu kena gempa besar, sekarang sudah pulih", klaim "sudah pulih" diuji lebih dulu lewat riset — dan ternyata tidak akurat. Data resmi awal 2026 menunjukkan pemulihan fisik memang signifikan (350.000+ rumah diserahkan) TAPI pemulihan sosial-ekonomi masih jauh dari tuntas (360.000 orang masih di hunian kontainer, pengangguran tinggi). Artikel ditulis dengan framing yang lebih presisi: **"pemulihan besar-besaran namun belum tuntas"**, bukan "sudah pulih". Prinsipal menerima framing yang lebih akurat ini. Pola ini harus terus dijalankan: klaim tentang kondisi/status terkini yang berpotensi berubah SELALU diverifikasi lewat pencarian sebelum ditulis sebagai fakta dalam artikel, sekalipun klaim itu datang dari prinsipal sendiri.

### 2.7 Verifikasi fakta khusus untuk artikel profil tokoh
Artikel profil paling sering kena koreksi pasca-terbit. Riwayat repo mencatat: artikel #054 (Don Hasman) butuh **dua commit koreksi fakta terpisah** setelah tayang (kekeliruan Nuptse vs Lhotse, dan kekeliruan durasi perjalanan). Untuk artikel profil, periksa ketat: nama gunung persis (termasuk ejaan diakritik), ketinggian dalam mdpl, tahun kejadian, dan jabatan resmi — jangan andalkan satu sumber saja kalau ada detail yang terasa janggal.

### 2.8 Kategori/tag yang dipakai di seluruh situs
`ORGANISASI` · `INTERNASIONAL` · `EKSPEDISI` · `KESELAMATAN` · `KERJASAMA` · `PELATIHAN` · `STANDARISASI` · `LINGKUNGAN` · `KOMPETISI`

Tombol filter di `berita/index.html` sudah memuat semua kategori ini. Atribut `data-category` pada tiap kartu index harus persis salah satu dari daftar di atas, huruf kapital semua, tanpa variasi ejaan.

### 2.9 Menangani foto berlisensi (Wikimedia Commons dkk.)
Kalau prinsipal tidak menyediakan foto sendiri untuk suatu artikel:
- Cari kandidat dari sumber aman: Wikimedia Commons (lisensi paling jelas), Pexels, Pixabay, Unsplash.
- **Hindari lisensi CC BY-SA (share-alike)** bila ada alternatif CC BY biasa yang setara kualitasnya — share-alike punya konsekuensi hukum yang lebih mengikat untuk situs yang menampungnya.
- **Atribusi wajib dicantumkan di caption artikel**: nama fotografer, sumber (Wikimedia Commons dll.), dan jenis lisensi persis (mis. "CC BY 4.0"). Contoh nyata dari artikel #061: *"Foto: Vyacheslav Argenberg / Wikimedia Commons (CC BY 4.0)"*.
- **Alur wajib:** cari beberapa kandidat → unduh kandidat-kandidat itu → tunjukkan opsinya ke prinsipal dengan pratinjau visual → prinsipal memilih → baru dipakai. **Jangan pernah memilih sendiri secara sepihak tanpa persetujuan eksplisit prinsipal**, sekalipun pilihannya tampak jelas dari sudut pandang teknis.

---

## 3. KEPUTUSAN YANG SUDAH DIAMBIL

Bagian ini mencatat keputusan konkret yang sudah final, supaya sesi baru tidak perlu menanyakan ulang atau — lebih buruk — membalik keputusan yang sudah disepakati.

### 3.1 Keputusan struktural/infrastruktur
| Keputusan | Rincian |
|---|---|
| Repo di-clone ke laptop operasional | `C:\Users\Admin\Documents\GitHub\berita-fmi` (sebelumnya belum pernah ada clone-nya di laptop ini sebelum sesi Juli 2026 dimulai). |
| Status akses push dikonfirmasi | Identitas GitHub `putrosm.darsono@gmail.com`, berstatus **collaborator** di repo organisasi `BeritaFMI`, terbukti bisa push langsung ke `main` — sudah diuji berkali-kali sepanjang beberapa sesi, selalu berhasil. |
| Register yang sempat korup, diperbaiki | Ekor `BERITA-REGISTER.md` (tabel backlog gambar untuk artikel #002–#010) sempat terpotong berulang kali karena kebiasaan menulis file tanpa newline penutup — korupsi ini sudah berlangsung sejak beberapa commit sebelum #057/#058, bukan insiden tunggal. Dipulihkan dengan mengambil badan register versi terkini + ekor backlog utuh dari commit lama (`a77fe3e`), lalu dijamin file selalu diakhiri newline tunggal. Commit perbaikan: `49f5428`. |
| Kartu #057 (Buyung Lalana) diperbaiki | Ditemukan dua masalah sekaligus: (1) path gambar salah, tertulis `berita/img/...` padahal `index.html` sudah berada *di dalam* folder `berita/`, sehingga path yang benar cukup `img/...` — kesalahan ini menyebabkan ikon broken-image di kartu; (2) struktur kartu memakai pola lama (`card-img-link`/`card-body`) yang berbeda dari kartu-kartu lain (`news-card--thumb`). Kedua masalah diperbaiki sekaligus, diseragamkan ke struktur standar terkini. Commit: `6a68b89`. Setelah perbaikan, seluruh 58+ kartu index sudah konsisten strukturnya — sudah diverifikasi tidak ada sisa path salah maupun struktur lama lainnya. |
| Nomor #044 sengaja dibiarkan bolong | Tidak ada file maupun baris register untuk nomor #044. **Ini disengaja dan dibiarkan — jangan pernah diisi ulang.** Penomoran artikel baru tetap maju dari nomor tertinggi yang ada (bukan mengisi nomor yang bolong di tengah). |
| Deploy Cloudflare untuk FMI lebih lambat dari portal saudara | Propagasi butuh sekitar 2 menit sebelum konten baru benar-benar tersaji di domain publik — lebih lambat dibanding HIFDI/Ummanitarian. Ini pola konsisten yang teramati berulang kali, bukan kejadian sekali waktu. |

### 3.2 Keputusan editorial per artikel (riwayat lengkap sesi Juli 2026)

**#059 — Khansa Syahlaa** (`059-khansa-syahlaa-pengurus-pb-fmi-seven-summits`)
- Tag `ORGANISASI`. Anchor jabatan yang dipakai: **Anggota Biro Humas & Koordinasi Wilayah PB FMI** — dikonfirmasi langsung oleh prinsipal karena tidak tersedia di sumber publik mana pun.
- Foto dari prinsipal (banner ucapan resmi FMI). Usia saat pendakian Carstensz 2017 sengaja tidak disebutkan (lihat Bagian 2.5). Angka jumlah gunung ditulis "sekitar 89 gunung, mayoritas di dalam negeri" (bukan "89 puncak dunia").

**#060 — Pernyataan Sikap FMI Jabar** (`060-fmi-jabar-pernyataan-sikap-keselamatan-pendakian`)
- Tag `ORGANISASI`. Sumber: pernyataan sikap resmi FMI Jabar menyusul diskusi publik bersama Mawara di Depok, Juli 2026.
- **Nomor HP narahubung DIMUAT** di badan artikel, atas keputusan eksplisit prinsipal (Fathur, FMI Jabar). Sebelumnya Sekjen sempat menyarankan untuk tidak memuat nomor HP demi menghindari risiko spam di halaman publik yang ter-index mesin pencari; prinsipal tetap memilih memuat nomornya. **Hormati keputusan ini** — jangan diam-diam dihapus di revisi mendatang tanpa alasan baru.
- Artikel ini memakai **dua foto**: foto utama (`060-fmi-jabar-pernyataan-sikap-keselamatan-pendakian.jpg`) dan foto sisipan di tengah badan artikel (`060-fmi-jabar-diskusi-pemateri.jpg`).
- Untuk mendukung foto sisipan, ditambahkan class CSS baru `.article-figure` (rincian lengkap CSS-nya ada di Bagian 4.6) — ini ekstensi minimal terhadap template standar, tidak mengubah bagian lain.
- Caption foto utama menyebutkan kehadiran langsung Ketua FMI Jawa Barat dr. Putro S. Muhammad, MH, CIHL dalam acara tersebut.

**#061 — UIAA General Assembly 2026** (`061-uiaa-general-assembly-2026-kathmandu`)
- Tag `INTERNASIONAL`.
- **FMI sama sekali tidak disinggung di badan artikel**, atas instruksi eksplisit prinsipal. Alasan pentingnya: verifikasi lapangan menunjukkan **FMI BUKAN anggota UIAA**. Yang terdaftar sebagai wakil Indonesia di direktori resmi UIAA adalah **Federasi Panjat Tebing Indonesia (FPTI)**, berstatus Active Member sejak 2016. **Jangan pernah** menulis atau menyiratkan FMI memiliki kursi, delegasi, atau keanggotaan di UIAA kecuali ada fakta baru yang benar-benar terverifikasi.
- Tanggal final yang dipakai (setelah proses verifikasi silang antar-halaman situs UIAA yang saling tidak konsisten, lihat Bagian 2.5): General Assembly **29–31 Oktober 2026**, Mountain Sports Symposium (edisi ketiga, fokus pendaki muda) **27–29 Oktober 2026**.
- Gambar: foto Mount Everest dari Wikimedia Commons, **CC BY 4.0, fotografer Vyacheslav Argenberg**. Atribusi lengkap dicantumkan di caption sesuai kewajiban Bagian 2.9.

**#062 — Tiga Tahun Setelah Gempa Turki** (`062-turki-pemulihan-gempa-perspektif-kebencanaan`)
- Tag `INTERNASIONAL`.
- **Framing utama diperbaiki dari bahan mentah prinsipal** — lihat Bagian 2.6. Bahan awal menyebut Turki "sekarang sudah pulih" dari gempa besar 6 Februari 2023; setelah verifikasi, framing final yang dipakai adalah **pemulihan besar-besaran namun belum tuntas** (350.000+ rumah sudah diserahkan, tapi 360.000 orang masih di hunian kontainer per awal 2026).
- **Judul dan hook sengaja diarahkan ke kondisi Turki**, bukan ke sosok Amar Haidar — prinsipal secara eksplisit meminta penyebutan Amar Haidar "menyublim" (muncul sekilas, tidak jadi subjek utama), dan hasil akhirnya Amar Haidar disebut di paragraf ketiga sebagai jembatan cerita, bukan di judul maupun paragraf pembuka.
- Jejak FMI dalam peristiwa 2023 disebut dengan nama lengkap sesuai yang diberikan prinsipal: **Widodo** dan **dr. Iqbal, Sp.B** di Kahramanmaraş; **dr. Putro S. Muhammad** di Hatay. Prinsipal sendiri disebut third-person murni, bukan "saya", meski beliau adalah prinsipal yang memberi instruksi.
- Magnitudo gempa: **7,7 (Pazarcık) dan 7,6 (Elbistan)**, dikonfirmasi dari AFAD (lihat Bagian 2.5).
- Ejaan nama tempat dikonfirmasi dari sumber resmi: **Kahramanmaraş** (dengan diakritik ş), **Hatay**.
- Caption foto TANPA menyebut nama kota di Turki (lokasi foto tidak dikonfirmasi prinsipal), sesuai keputusan eksplisit: *"Anggota FMI Jawa Barat Amar Haidar saat berada di Turki. Foto: Dokumentasi FMI Jawa Barat"*.
- **Catatan proses yang penting untuk diketahui:** saat artikel ini dikerjakan, sempat ditemukan bahwa file artikel, gambar, dan sebagian perubahan index/register **sudah ada di working directory secara utuh namun belum ter-commit ke git** — kemungkinan sisa proses sebelumnya yang terputus. Sebelum dipakai, seluruh isi file diverifikasi detail per detail terhadap draf final yang sudah di-acc prinsipal (judul, framing, magnitudo, posisi penyebutan Amar Haidar, ejaan nama tempat, caption) — barulah setelah cocok semua, dilanjutkan proses commit & push seperti biasa. **Pelajaran untuk sesi mendatang:** kalau menemukan file yang sudah "siap pakai" di working directory tapi berstatus untracked di git, JANGAN langsung dipercaya dan dipakai — selalu verifikasi isinya secara menyeluruh dulu terhadap keputusan editorial yang sudah disepakati, karena bisa jadi itu sisa draf lama yang belum sempat direvisi.
- Sempat terjadi juga insiden **Desktop Commander (MCP tool untuk kontrol laptop) macet total** di tengah proses push — proses `git push` sempat terkirim tapi outputnya tidak terbaca karena tool crash. Setelah tool di-restart oleh prinsipal, dicek ulang lewat `git log` lokal vs `origin/main`, dan ternyata push-nya **sudah berhasil** sebelum tool macet (commit hash lokal dan remote sama persis). **Pelajaran:** kalau tool sempat macet setelah perintah push dikirim, jangan asumsikan gagal atau berhasil — selalu verifikasi ulang dengan membandingkan `git log --oneline -1` lokal dengan `git log --oneline -1 origin/main` (setelah `git fetch`) begitu tool pulih.

### 3.3 Keputusan soal sumber gambar berlisensi
- File gambar **selalu disimpan lokal** di `berita/img/`, **bukan hotlink** ke URL eksternal. Ini berbeda dari portal Ummanitarian yang memang hotlink ke Pexels/Unsplash — jangan disamakan.
- Sumber gambar yang dianggap aman: Wikimedia Commons (paling disukai karena kejelasan lisensi), Pexels, Pixabay, Unsplash.
- Ekstensi gambar selalu `.jpg`, diproses ulang (resize + kompresi, biasanya kualitas 86–88, upscale ke sekitar 1280px lebar bila sumber lebih kecil dari 1200px) sebelum disimpan ke repo — jangan menyimpan file sumber mentah apa adanya.

### 3.4 Dokumen serah-terima sebelumnya (AGENTS.md)
Sebelum dokumen `fmi.md` ini dibuat, sempat ditulis draf serah-terima dengan nama `AGENTS.md` langsung di root repo (`C:\Users\Admin\Documents\GitHub\berita-fmi\AGENTS.md`). File itu **masih berstatus untracked di git** (belum pernah di-commit) karena keputusan commit-atau-tidaknya belum diambil prinsipal saat itu. Dokumen `fmi.md` ini adalah **versi yang lebih lengkap dan menggantikan** isi `AGENTS.md` tersebut — nama sengaja diganti menjadi `fmi.md` atas permintaan eksplisit prinsipal, supaya tidak tertukar dengan file `AGENTS.md` milik repo lain yang mungkin ditangani bridge DeepSeek di direktori kerja yang sama. **Perlu diputuskan oleh prinsipal:** apakah file `AGENTS.md` yang lama di root repo dihapus/dibiarkan, dan apakah `fmi.md` ini disimpan di dalam repo (dan kalau ya, di-commit atau dibiarkan lokal saja) atau cukup disimpan di luar repo sebagai referensi kerja.

---

## 4. KONTEKS & INFRASTRUKTUR

### 4.1 Rantai penerbitan (end-to-end)
```
Laptop operasional (C:\Users\Admin\Documents\GitHub\berita-fmi)
  → git commit + git push
  → GitHub: organisasi BeritaFMI, repo berita-fmi, branch main
  → GitHub Actions (.github/workflows/deploy.yml) terpicu otomatis oleh push ke main
  → Cloudflare Pages (project: berita-fmi)
  → https://berita.mountaineering-indonesia.org
```

### 4.2 Isi `deploy.yml` (sudah terverifikasi bekerja, JANGAN diubah tanpa alasan kuat)
```yaml
name: Deploy to Cloudflare Pages
on:
  push:
    branches: [main]
  workflow_dispatch:
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Deploy to Cloudflare Pages
        uses: cloudflare/wrangler-action@v3
        with:
          apiToken: ${{ secrets.CLOUDFLARE_API_TOKEN }}
          accountId: ${{ secrets.CLOUDFLARE_ACCOUNT_ID }}
          command: pages deploy berita --project-name=berita-fmi --branch=main
```
Konsekuensi paling penting dari baris perintah terakhir: **hanya isi folder `berita/` yang benar-benar di-deploy ke Cloudflare**, dan folder itu sendiri yang menjadi root situs publik (bukan root repo).

### 4.3 Struktur repo — bagian-bagian yang berpotensi menjebak
| Path | Status & catatan |
|---|---|
| `berita/` | **KANONIK.** Semua konten yang benar-benar tayang hidup di sini. |
| `berita/index.html` | Halaman depan situs publik. **Berada DI DALAM folder `berita/`**, sehingga path gambar yang ditulis di dalamnya cukup `img/...` — **BUKAN** `berita/img/...`. Kekeliruan menulis path dengan prefix `berita/` inilah yang pernah merusak kartu #057 (lihat Bagian 3.1). |
| `berita/img/` | Lokasi semua gambar artikel, termasuk `fmi-logo.jpg` yang dipakai di navigasi tiap halaman. |
| File `*.html` di ROOT repo (mis. `001-....html` hingga sekitar `045-....html`) | **SISA LAMA. JANGAN PERNAH DIEDIT.** Isinya berbeda dari versi yang ada di `berita/`, dan **tidak ikut ter-deploy sama sekali**. Kalau ada permintaan mengedit artikel lama bernomor kecil, pastikan dulu file yang diedit ada di `berita/`, bukan di root. |
| `BERITA-REGISTER.md` di ROOT repo | **REGISTER AKTIF, sumber kebenaran tunggal untuk penomoran artikel.** |
| `_meta/BERITA-REGISTER.md` | **BASI, jangan dipakai.** Berhenti diperbarui sejak next=036. Kalau sesi baru secara tidak sengaja membaca file register dari sini, seluruh nomor artikel akan salah total. |
| `_operasional/DESAIN-SISTEM.md` | Dokumen desain sistem visual situs. Baca lebih dulu sebelum melakukan perubahan tampilan/CSS yang signifikan. |
| `.github/workflows/deploy.yml` | Workflow deploy, sudah diverifikasi berfungsi normal berkali-kali. |
| `AGENTS.md` (di root repo, kalau masih ada) | Draf serah-terima versi sebelumnya, digantikan oleh `fmi.md` ini — lihat Bagian 3.4 untuk status dan keputusan yang masih menggantung soal file ini. |

### 4.4 Akun & akses
- Identitas GitHub operator laptop: **putrosm.darsono@gmail.com**, berstatus **collaborator** pada repo organisasi `BeritaFMI` — sudah terbukti bisa push langsung ke `main` berkali-kali di berbagai sesi.
- **Ada editor lain yang aktif secara independen: akun `sekretariatanfmi`.** Karena itu, **`git pull` WAJIB dijalankan di awal setiap sesi kerja dan sebelum tiap artikel baru** — jangan berasumsi kondisi repo sama seperti sesi sebelumnya.
- Cloudflare account id (terlihat dari URL dashboard): `bd21dc6db0d6774e7f8dc0a2a40b6293`. Nama project: `berita-fmi`. Dashboard Cloudflare belum pernah diperiksa langsung sepanjang sesi-sesi ini — tidak mendesak untuk dicek, karena rantai deploy sudah berulang kali terbukti bekerja lewat verifikasi hasil tayang di domain publik.
- Secrets `CLOUDFLARE_API_TOKEN` dan `CLOUDFLARE_ACCOUNT_ID` tersimpan di pengaturan GitHub Actions repo (bukan di kode), dan masih valid per commit terakhir yang sudah diverifikasi tayang.

### 4.5 Alur publish standar, langkah demi langkah
1. **`git pull`** di root repo — wajib tanpa kecuali, karena ada editor lain yang aktif.
2. **Tentukan nomor artikel & kunci slug final.** Baca angka "Next Available Number" di `BERITA-REGISTER.md` yang ada di ROOT (bukan yang di `_meta/`), lalu cek silang nomor tertinggi yang benar-benar ada sebagai file di folder `berita/` — pakai yang lebih tinggi di antara keduanya sebagai nomor yang dipakai. **Kunci slug (nama file) final SEBELUM membuat file apa pun.** Riwayat repo mencatat beberapa commit "fix: hapus duplikat" di sekitar artikel #052 akibat slug yang berubah di tengah proses penulisan, meninggalkan file lama yang harus dihapus lewat commit terpisah — hindari pengulangan kesalahan ini.
3. **Tulis artikel dwibahasa penuh** sesuai seluruh aturan di Bagian 2, sambil menyiapkan gambar (lokal, sudah diproses ulang) di `berita/img/`.
4. **Salin struktur HTML dari artikel TERBARU yang benar-benar ada di repo** — jangan pernah mereka-reka struktur dari ingatan sesi sebelumnya, karena template bisa saja sudah mengalami penyesuaian kecil (lihat contoh penambahan class `.article-figure` di #060). Setelah itu, perbarui `berita/index.html` (kartu artikel baru selalu ditambahkan di posisi PALING ATAS, tepat setelah pembuka `<main class="news-grid">`) dan `BERITA-REGISTER.md` (tambah satu baris baru di posisi paling atas tabel + naikkan angka "Next Available Number").
5. **Publish dengan 4 commit granular** (urutan dan format persis di Bagian 4.9), lalu push, lalu WAJIB verifikasi hasil tayang di domain publik (Bagian 4.10) sebelum menganggap pekerjaan selesai.

### 4.6 Anatomi lengkap satu file artikel
Nama file mengikuti pola: `berita/{NNN}-{slug-deskriptif}.html`

Urutan blok di dalam file:

1. **`<head>`**: `<title>`, meta description, kelompok meta Open Graph lengkap (`og:type`, `og:url`, `og:title`, `og:description`, `og:image`, `og:locale`, `og:site_name`), kelompok meta Twitter Card (`twitter:card`, `twitter:title`, `twitter:image`), `<link rel="canonical">`, preconnect ke Google Fonts, pemanggilan tiga font (Bebas Neue untuk display, Crimson Pro untuk badan artikel, DM Sans untuk UI), lalu blok `<style>`.

2. **CSS custom properties** yang dipakai konsisten di semua artikel:
   ```css
   --red: #C8102E; --black: #111111; --white: #FFFFFF;
   --white-off: #F8F7F5; --gray-light: #EBEBEB; --gray-mid: #888888;
   --text-main: #111111; --text-sub: #444444;
   ```
   Tiga variabel font: `--font-display` (Bebas Neue), `--font-serif` (Crimson Pro, dipakai badan artikel), `--font-body` (DM Sans, dipakai UI/navigasi).

3. **Mekanisme toggle bahasa**, murni lewat CSS berbasis class pada `<body>`:
   ```css
   [data-en] { display: none; }
   .lang-en [data-id] { display: none; }
   .lang-en [data-en] { display: revert; }
   .lang-id [data-id] { display: revert; }
   .lang-id [data-en] { display: none; }
   ```

4. `<body class="lang-id">` — bahasa Indonesia selalu jadi default saat halaman pertama dimuat.

5. **`<nav>`**: logo (`img/fmi-logo.jpg`) yang mengarah ke `https://mountaineering-indonesia.org`, tiga tautan navigasi (Beranda/Home, Berita/News, Kontak/Contact — masing-masing dengan pasangan `data-id`/`data-en`), dan `.lang-toggle` berisi dua tombol `#btn-id` dan `#btn-en` yang memanggil fungsi JavaScript `setLang()`.

6. **`.article-header`**: berisi `.back-link` (tautan "← Kembali ke Berita" / "← Back to News"), `.article-meta` (terdiri dari `.article-tag` untuk kategori, `.article-source` selalu bertuliskan "Berita FMI", `.article-dot` sebagai pemisah visual, dan `.article-date` dengan pasangan ID/EN), lalu **dua** elemen `<h1 class="article-title">` — satu dengan atribut `data-id`, satu dengan `data-en`.

7. **`.article-photo`**: berisi satu `<img>` yang menunjuk ke `img/{NNN}-{slug}.jpg`, dengan `object-fit: contain` supaya foto tidak terpotong paksa.

8. **`.article-caption`**: dua `<span>` (ID dan EN) berisi keterangan foto, termasuk kredit fotografer/sumber/lisensi kalau foto berasal dari sumber berlisensi eksternal (lihat Bagian 2.9).

9. **`.article-wrap`** membungkus **`.article-body`**, yang berisi pasangan-pasangan `<p data-id>` dan `<p data-en>` untuk seluruh isi artikel. Pemisah visual opsional `<div class="article-divider"></div>` dipakai di antara bagian "fakta" dan bagian "makna/pointer" pada beberapa artikel untuk memberi jeda visual.

10. **`<footer>`** berisi copyright dan tautan balik ke situs utama, diikuti **`<script>`** berisi fungsi `setLang(lang)` yang mengganti `className` pada `<body>` dan status `active` pada dua tombol toggle bahasa.

**Foto sisipan di tengah badan artikel** (pertama kali dipakai di artikel #060, class tambahan terhadap template dasar):
```css
.article-figure { margin: 2.5rem 0; }
.article-figure img { width: 100%; display: block; border: 1px solid var(--gray-light); }
.article-figure figcaption { font-size: 0.82rem; color: var(--gray-mid); font-style: italic; margin-top: 0.6rem; }
```
```html
<figure class="article-figure">
  <img src="img/{NNN}-{slug-sisipan}.jpg" alt="...">
  <figcaption data-id>...</figcaption>
  <figcaption data-en>...</figcaption>
</figure>
```

### 4.7 Anatomi kartu di halaman index
Kartu baru selalu disisipkan **tepat setelah** pembuka `<main class="news-grid">`, sehingga artikel terbaru selalu tampil paling atas:
```html
<article data-category="KATEGORI" class="news-card news-card--thumb reveal">
  <div class="card-thumb">
    <img src="img/{NNN}-{slug}.jpg" alt="..." loading="lazy">
  </div>
  <div class="card-content">
    <div class="card-meta">
      <span class="card-tag" style="background:#C8102E">KATEGORI</span>
      <span class="card-source">Berita FMI</span>
      <span class="card-dot">·</span>
      <span class="card-date" data-id>21 Juli 2026</span>
      <span class="card-date" data-en>July 21, 2026</span>
    </div>
    <h2 class="card-title">
      <span data-id>Judul versi Indonesia</span>
      <span data-en>English title</span>
    </h2>
    <p class="card-desc" data-id>Ringkasan singkat versi Indonesia.</p>
    <p class="card-desc" data-en>Short English summary.</p>
    <a class="card-link" href="{NNN}-{slug}.html" target="_blank">
      <span data-id>Baca Selengkapnya</span><span data-en>Read More</span>
      <span class="link-arrow">↗</span>
    </a>
  </div>
</article>
```
Elemen yang wajib ada dan sering terlupa: atribut `data-category` (dipakai mekanisme filter kategori di halaman), class `reveal` (memicu animasi saat kartu discroll ke area pandang), path gambar dengan awalan `img/...` saja (bukan `berita/img/...`, lihat Bagian 4.3), dan atribut `loading="lazy"` pada `<img>`.

### 4.8 Format `BERITA-REGISTER.md`
Field paling atas yang harus selalu diperbarui begitu nomor baru diambil:
```
## ⚡ Next Available Number: **NNN**
```

Format satu baris tabel (baris terbaru selalu ditambahkan paling atas, tepat di bawah baris header tabel):
```
| 062 | `062-turki-pemulihan-gempa-perspektif-kebencanaan.html` | Tiga Tahun Setelah Gempa "Bencana Abad Ini", Kondisi Turki Kini | 29 Jul 2026 | INTERNASIONAL | Sekjen | Lokal |
```
Urutan kolom: No | Slug/URL | Judul (ringkas) | Tanggal | Tag | Penulis | Tipe.

**Selalu jaga agar file diakhiri newline tunggal setelah baris terakhir.** Riwayat repo menunjukkan ekor file ini berulang kali terpotong secara tidak sengaja karena kebiasaan menulis file tanpa newline penutup yang konsisten — ini pernah butuh perbaikan khusus (Bagian 3.1). Setelah menambah baris baru, ada baiknya cek eksplisit dengan membaca beberapa baris terakhir file untuk memastikan tidak ada yang terpotong.

### 4.9 Konvensi commit (granular, selalu 4 commit terpisah per artikel)
Urutan dan format pesan commit yang konsisten dipakai di seluruh riwayat repo:
```
feat: artikel #NNN - <judul ringkas>
feat: gambar artikel #NNN - <keterangan singkat isi gambar>
feat: tambah card artikel #NNN - <judul ringkas> di index
chore: update register - artikel #NNN, next=NNN+1
```
**Sebelum setiap commit**, jalankan `git status --short` dan pastikan hanya file yang memang dimaksud yang berstatus berubah — ini mencegah file lain (misalnya perubahan tak sengaja atau sisa proses lain) ikut ter-commit tanpa disadari.

### 4.10 Verifikasi wajib pasca-push
Jangan pernah menganggap artikel selesai hanya karena `git push` tidak menampilkan pesan error. Langkah verifikasi yang wajib dilakukan:
- **Tunggu propagasi deploy sekitar 2 menit** sebelum mengecek (lebih lambat dibanding HIFDI/Ummanitarian, ini pola konsisten yang sudah berulang kali teramati). Cek pertama sering kali masih menyajikan konten lama — ini normal, bukan tanda kegagalan; tunggu dan cek ulang.
- **URL artikel yang live selalu TANPA akhiran `.html`** — Cloudflare Pages melakukan redirect 308 dari URL berakhiran `.html` ke versi tanpa akhiran. Gunakan URL tanpa `.html` saat verifikasi supaya tidak salah membaca hasil sebagai kegagalan.
- **Selalu tambahkan cache-bust** berupa query string `?v=<timestamp-unix>` pada tiap pengecekan, supaya tidak membaca hasil cache lama.
- Periksa berurutan: (1) HTTP 200 pada URL artikel, (2) beberapa penanda konten khas yang unik untuk artikel tersebut benar-benar muncul di HTML yang diterima (bukan sekadar HTTP 200 — halaman error kustom pun bisa mengembalikan 200), (3) HTTP 200 pada seluruh file gambar yang dipakai artikel, (4) halaman index memuat slug artikel baru di dalam HTML-nya.
- Kalau `git push` sempat terkirim namun hasilnya tidak jelas (misalnya karena tool sempat crash seperti kasus artikel #062 di Bagian 3.2), **jangan asumsikan gagal maupun berhasil** — verifikasi dengan `git fetch` lalu bandingkan `git log --oneline -1` lokal terhadap `git log --oneline -1 origin/main`. Kalau hash-nya sama, push sudah berhasil; kalau beda, ulangi `git push`.

---

## 5. PEKERJAAN BERJALAN

**Status per penulisan dokumen ini (29 Juli 2026):**
- Artikel terakhir yang tayang: **#062** — "Tiga Tahun Setelah Gempa 'Bencana Abad Ini', Bagaimana Kondisi Turki Kini" (`062-turki-pemulihan-gempa-perspektif-kebencanaan.html`), tag `INTERNASIONAL`, sudah terverifikasi tayang di domain publik (HTTP 200, penanda konten cocok, gambar termuat, kartu index memuat slug artikel).
- **Next Available Number di register: 063.** Artikel berikutnya yang ditulis harus memakai nomor ini (dengan tetap melakukan cek silang ke folder `berita/` sesuai Bagian 4.5 langkah 2, untuk berjaga-jaga kalau editor lain `sekretariatanfmi` sudah menerbitkan sesuatu di antara waktu penulisan dokumen ini dan sesi berikutnya).
- **Status commit lokal vs remote: sinkron.** HEAD lokal dan `origin/main` sama-sama berada di commit `384485b` ("chore: update register - artikel #062, next=063") pada saat dokumen ini ditulis.
- **Status `git status --short` repo pada saat dokumen ini ditulis:** hanya satu file berstatus untracked, yaitu `AGENTS.md` di root repo (dokumen serah-terima versi sebelumnya, lihat Bagian 3.4). Tidak ada file lain yang tertinggal dalam kondisi setengah-commit.
- **Lima artikel terakhir secara berurutan** (untuk konteks pola topik & tag yang baru saja dipakai, supaya artikel berikutnya bisa memberi variasi): #062 Turki/INTERNASIONAL, #061 UIAA/INTERNASIONAL, #060 FMI Jabar/ORGANISASI, #059 Khansa Syahlaa/ORGANISASI, #058 Liliya Ianovskaia/INTERNASIONAL. Tiga dari lima artikel terakhir bertag INTERNASIONAL — kalau ada bahan dengan tag lain (EKSPEDISI, KESELAMATAN, KERJASAMA, dll.) ada baiknya diprioritaskan untuk variasi, walau ini bukan aturan keras, murni pertimbangan keberagaman konten.

**Yang BELUM dikerjakan / masih menggantung:**
- Keputusan final soal file `AGENTS.md` lama di root repo — dihapus, dibiarkan, atau digabung isinya ke `fmi.md` lalu dihapus (lihat Bagian 3.4 dan Action Item di bagian penutup).
- Keputusan apakah `fmi.md` ini sendiri disimpan di dalam repo (dan kalau ya, apakah di-commit ke git atau disimpan lokal saja di luar tracking git) atau cukup disimpan di luar repo sebagai referensi kerja bridge DeepSeek.
- Belum ada artikel yang disiapkan/didraf untuk nomor #063 — sesi berikutnya mulai dari nol untuk topik berikutnya, menunggu bahan dari prinsipal.

---

## 6. ALUR DISTRIBUSI WHATSAPP

**Aturan tetap (berlaku otomatis, tanpa perlu diminta ulang setiap kali):** setiap artikel Berita FMI yang selesai tayang dan sudah terverifikasi live, **selalu** disertai satu caption siap-share untuk WhatsApp Group segera setelah proses verifikasi tayang selesai — tidak perlu menunggu diminta oleh prinsipal.

**Format caption yang sudah dipakai konsisten** (contoh nyata dari artikel-artikel yang sudah tayang):
```
🏔️/🇹🇷/🩺/⛰️ (emoji tematik sesuai isi berita) *Judul ringkas dalam format bold WhatsApp*

Ringkasan inti dalam 1–2 kalimat, mengambil poin paling menarik/penting dari artikel — bukan sekadar mengulang judul.

(Opsional) Satu paragraf tambahan berisi detail pendukung yang menarik perhatian, misalnya rangkaian fakta/tanggal/angka, atau kutipan poin penting.

Selengkapnya (ID/EN):
https://berita.mountaineering-indonesia.org/{NNN}-{slug}
```
Catatan format:
- Emoji dipilih sesuai tema (gunung, bendera negara, simbol medis, dll.) — bukan emoji acak, dan hanya satu di awal caption.
- Judul selalu diapit tanda bintang tunggal (format bold WhatsApp: `*teks*`).
- Tautan artikel **selalu tanpa akhiran `.html`** (mengikuti pola URL live yang benar, lihat Bagian 4.10) dan selalu ditandai "(ID/EN)" karena setiap artikel memang dwibahasa dengan toggle di halamannya.
- Bahasa caption sendiri: Indonesia, singkat, faktual — tanpa hiperbola atau bahasa promosi berlebihan, konsisten dengan nada editorial keseluruhan situs (Bagian 2.1).
- Panjang caption tidak dipatok kaku, tapi pola yang sudah berjalan: 3–5 baris paragraf pendek sebelum tautan, disesuaikan kepadatan informasi tiap artikel (artikel dengan poin lebih banyak, seperti pernyataan sikap organisasi, bisa memakai satu paragraf tambahan; artikel dengan satu ide inti, seperti profil tokoh, cukup satu paragraf ringkasan).

**Timing:** caption disusun dan disajikan ke prinsipal **sekali per artikel**, langsung menyatu dengan laporan hasil verifikasi tayang — tidak dipisah jadi permintaan/tahap terpisah, dan tidak ditunda ke pesan berikutnya.

**Belum ditentukan/belum diketahui** (perlu diklarifikasi ke prinsipal kalau relevan di kemudian hari): nama/identitas grup WhatsApp tujuan spesifik tidak pernah disebutkan eksplisit dalam sesi-sesi sejauh ini — caption disiapkan sebagai teks siap-copy, pengiriman aktual ke grup dilakukan manual oleh prinsipal sendiri, bukan oleh Sekjen.

---

## 6b. DISTRIBUSI OTOMATIS via OpenWA (loop tertutup, bridge DeepSeek)

Sebelumnya caption dikirim manual oleh prinsipal (bagian 6). Di bridge DeepSeek langkah ini bisa otomatis lewat gateway OpenWA lokal. Grup tujuan kini **sudah dikonfirmasi**.

**Grup tujuan:** Media Centre FMI -> `120363411322888897@g.us`

**Gateway:** OpenWA lokal di Docker, `http://localhost:2785`. Shell bridge DeepSeek jalan di mesin lokal, jadi bisa nyapa localhost langsung (sama seperti `git push`).

**Prasyarat sebelum kirim:**
- Docker Desktop nyala + container `openwa-api` Up (`docker ps`).
- Session `berita-wa` `status: ready`.
- Artikel SUDAH terverifikasi live (URL tanpa `.html`, HTTP 200) sebelum caption dikirim. Jangan kirim caption sebelum tayang beneran.

**Kredensial DIPISAH ke file `wa-config.local.ps1`** (gitignored — WAJIB. Repo publik + aturan keras "tidak ada kredensial di file repo"). JANGAN pernah tulis API key OpenWA di fmi.md / AGENTS.md / file mana pun yang bisa ter-commit.

**Perintah kirim (PowerShell):**
```powershell
. .\wa-config.local.ps1   # muat kredensial OpenWA (file gitignored)
$h = @{ "X-API-Key"=$OPENWA_KEY; "Content-Type"="application/json" }
$b = @{ chatId=$FMI_GROUP; text=$captionText } | ConvertTo-Json
Invoke-RestMethod -Uri "$OPENWA_URL/api/sessions/$OPENWA_SESSION/messages/send-text" -Method Post -Headers $h -Body $b
```

**Catatan caption:** caption FMI pakai emoji tematik + bold WhatsApp `*teks*` + dwibahasa (bagian 6). Kirim teks caption apa adanya; emoji & baris kosong aman lewat `ConvertTo-Json`. Untuk caption dwibahasa, kirim versi Indonesia (atau gabungan ID/EN sesuai kebiasaan grup Media Centre FMI).

**Verifikasi:** respons berisi `id`/`timestamp` tanpa error = terkirim. Cek juga pesan nongol di grup Media Centre FMI.

**Safe-send:** OpenWA unofficial, ada risiko ban. Nomor gateway (62895615779993) = nomor buangan. Satu grup Media Centre FMI per artikel; jangan blast banyak grup sekaligus.

---

## 6c. BRIDGE TELEGRAM (`@beritaFMI_bot`) — akses Sekjen dari HP

Dibangun 3–4 Agustus 2026. Prinsipal bisa chat dengan Sekjen kapan saja lewat
Telegram (`@beritaFMI_bot`) — setor ide artikel, kirim foto amunisi gambar,
minta status, sampai minta commit+push+kirim WA langsung dari HP tanpa buka
laptop.

**Kode & rencana desain lengkap** (di luar repo `berita-fmi`, bukan bagian
konten publik ini): `C:\Users\Admin\berita-bridge\` (bridge bersama 3 portal, engine DeepSeek).
Rencana arsitektur lama: arsip di `C:\Users\Admin\berita-bridge\`.

**Cara kerja singkat:** long-polling Telegram → filter satu ID Telegram
prinsipal (`446614920`, yang lain didiamkan total) → bridge DeepSeek headless di
repo ini (stateless; konteks diambil dari AGENTS.md + SEKJEN.md tiap pesan) →
balasan dikirim balik ke Telegram.

**Keputusan risiko sadar (jangan diubah tanpa didiskusikan ulang):** jalan
dengan `--dangerously-skip-permissions` — semua aksi (commit, push, kirim
WA) otomatis tanpa jeda konfirmasi, atas permintaan eksplisit prinsipal
setelah risikonya disampaikan jelas (dokumentasi flag itu sendiri
menyarankan hanya dipakai di sandbox tanpa internet). Satu-satunya gerbang
adalah filter ID Telegram di atas.

**Gaya komunikasi di sesi bridge ini WAJIB ikut bagian 1** (uji sekali,
ringkas, lalu jalan — bukan interogasi berlapis). Sesi headless yang
di-spawn bridge tidak mewarisi kalibrasi dari sesi panjang mana pun, jadi
kepatuhan ke bagian 1 di sini krusial, bukan opsional.

---

## 7. HAL YANG MUDAH TERLUPA

Daftar ringkas hal-hal yang sudah terbukti menyebabkan kesalahan di sesi-sesi sebelumnya, dikumpulkan di satu tempat sebagai pengingat cepat:

1. **Path gambar di `berita/index.html` cukup `img/...`, BUKAN `berita/img/...`** — karena file index.html itu sendiri sudah ada di dalam folder `berita/`. Ini pernah merusak kartu #057.
2. **Register yang benar ada di ROOT repo** (`BERITA-REGISTER.md`), **bukan** yang di `_meta/` (basi, berhenti di next=036).
3. **File `*.html` bernomor kecil di ROOT repo adalah sisa lama yang tidak ikut ter-deploy** — jangan pernah diedit, konten asli yang tayang selalu ada di dalam folder `berita/`.
4. **Selalu `git pull` di awal sesi dan sebelum tiap artikel baru** — ada editor lain (`sekretariatanfmi`) yang bisa saja sudah menerbitkan sesuatu tanpa sepengetahuan sesi ini.
5. **URL artikel yang live selalu tanpa akhiran `.html`** (redirect 308 dari Cloudflare Pages) — jangan salah membaca ini sebagai kegagalan deploy saat verifikasi.
6. **Propagasi deploy FMI butuh sekitar 2 menit**, lebih lambat dari portal saudara — jangan panik dan jangan langsung push ulang kalau cek pertama masih menampilkan versi lama.
7. **Setiap elemen teks di artikel wajib berpasangan `data-id` dan `data-en`** — termasuk elemen yang gampang terlewat seperti judul H1, caption foto, figcaption foto sisipan, dan label tombol. Validasi teknis (hitung jumlah kemunculan `data-id` vs `data-en`, harus seimbang) sebaiknya dilakukan tiap kali sebelum commit.
8. **Nomor artikel #044 sengaja dibiarkan bolong** — jangan pernah diisi ulang, penomoran tetap maju dari nomor tertinggi yang ada.
9. **File yang sudah "siap pakai" tapi berstatus untracked di git jangan langsung dipercaya** — selalu verifikasi isinya cocok dengan keputusan editorial yang sudah disepakati sebelum dipakai untuk commit (lihat kasus nyata di artikel #062, Bagian 3.2).
10. **Kalau tool kontrol laptop (Desktop Commander atau sejenisnya) sempat crash setelah perintah `git push` dikirim**, jangan asumsikan berhasil atau gagal — selalu verifikasi ulang dengan membandingkan hash commit lokal dan remote setelah tool pulih.
11. **Klaim tentang kondisi/status terkini yang datang dari prinsipal sekalipun tetap perlu diverifikasi** sebelum ditulis sebagai fakta di artikel — lihat kasus "Turki sudah pulih" yang ternyata perlu framing lebih presisi (Bagian 2.6).
12. **FMI bukan anggota UIAA** — jangan pernah menuliskan atau menyiratkan sebaliknya di artikel bertema UIAA di masa depan, kecuali ada fakta baru yang benar-benar terverifikasi ulang.
13. **Jangan pernah membuat file HTML/MD/produk apa pun di repo tanpa acc eksplisit dari prinsipal terlebih dahulu** — ini aturan keras yang berlaku selalu, tanpa pengecualian untuk alasan apa pun termasuk urgensi.

---

## ACTION ITEM YANG BELUM SELESAI

- [ ] **Putuskan nasib file `AGENTS.md` lama** di root repo (`C:\Users\Admin\Documents\GitHub\berita-fmi\AGENTS.md`, masih untracked, belum pernah di-commit) — hapus, biarkan, atau isinya digabung penuh ke sini lalu file lama dihapus.
- [ ] **Putuskan status `fmi.md` ini sendiri**: disimpan di dalam repo (dan kalau ya, apakah di-commit ke git yang publik, atau disengaja dibiarkan di luar tracking git) — atau cukup disimpan di luar repo sebagai referensi kerja lokal untuk bridge DeepSeek saja.
- [ ] **Artikel #064 belum ada bahan/topik.** Menunggu arahan/bahan dari prinsipal untuk konten berikutnya. (Artikel #063 — Nirmal Purja — sudah tayang 1 Agustus 2026.)
- [ ] **Dashboard Cloudflare belum pernah diperiksa langsung** (nama project persis, status connect domain, riwayat deployment). Belum mendesak karena rantai deploy sudah berulang kali terbukti bekerja, tapi baik untuk dicek sesekali sebagai audit kesehatan sistem, terutama kalau suatu saat propagasi terasa jauh lebih lambat dari biasanya atau ada laporan halaman tidak update.
- [ ] **Keanggotaan organisasi GitHub `BeritaFMI` belum pernah diperiksa detail lewat antarmuka organisasi** (siapa saja member/owner selain `putrosm.darsono` dan `sekretariatanfmi` yang sudah diketahui aktif) — tidak mendesak karena akses push sudah terbukti bekerja, tapi relevan untuk diketahui kalau suatu saat perlu mengatur ulang akses atau menambah kolaborator baru.
- [ ] **Uji cold-start `AGENTS.md` secara berkala** — buka sesi baru tanpa memori sama sekali, biarkan baca dokumen ini sendiri lalu lanjutkan kerja tanpa bantuan tambahan, untuk menemukan bagian yang sudah usang atau kurang jelas sebelum jadi masalah nyata. Pola ini diambil dari pengalaman kantor berita saudara (HIFDI, Agustus 2026): dokumentasi yang belum pernah diuji "orang baru datang, baca ini, jalan sendirian" kelihatannya lengkap sampai benar-benar dicoba.
- [ ] **Cadangkan konfigurasi gateway OpenWA (sesi `berita-wa`)** — saat ini hanya hidup di satu laptop (`C:\Users\Admin\Documents\GitHub\berita-fmi` beserta container Docker-nya). Kalau laptop ini rusak atau hilang, sesi WhatsApp yang sudah ter-autentikasi ikut hilang total dan harus scan QR ulang dari nol di nomor gateway yang sama. Belum ada rencana cadangan di luar laptop ini.

---

## RINGKASAN SATU LAYAR

Berita FMI (`berita.mountaineering-indonesia.org`) adalah portal berita bilingual (ID/EN) milik Federasi Mountaineering Indonesia, dikelola dr. Putro S. Muhammad (panggil **"Anda"**, jangan "situ") lewat repo GitHub organisasi `BeritaFMI/berita-fmi`, dengan alur `git push` → GitHub Actions → Cloudflare Pages, deploy dari isi folder `berita/` (bukan root repo). Konten kanonik hanya di `berita/`; register aktif adalah `BERITA-REGISTER.md` di root (**next number saat ini: 064**). Setiap artikel wajib dwibahasa penuh (pasangan `data-id`/`data-en` di tiap elemen), gaya third-person murni tanpa metafora/klaim subjektif, tanpa bagian "sikap organisasi" ala HIFDI, dan setiap fakta harus terverifikasi — termasuk kalau klaimnya datang dari prinsipal sendiri. Publish selalu 4 commit granular (artikel → gambar → kartu index → register), didahului `git pull` (ada editor lain, `sekretariatanfmi`), diakhiri verifikasi tayang di domain publik (URL tanpa `.html`, tunggu ±2 menit propagasi, cache-bust `?v=timestamp`) dan pengiriman caption WhatsApp otomatis lewat gateway OpenWA (bagian 6b) ke grup Media Centre FMI, tanpa diminta. Artikel terakhir yang tayang: **#063**, soal meninggalnya Nirmal Purja dalam longsoran Broad Peak, Pakistan. Aturan paling keras yang tidak boleh dilanggar dalam kondisi apa pun: **jangan pernah membuat file di repo tanpa acc eksplisit dari prinsipal**, dan **jangan pernah menuliskan klaim afiliasi organisasi (termasuk keanggotaan UIAA) yang tidak benar-benar terverifikasi**.
