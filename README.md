# BooKil Day 2 — Hands On: Project Pertamamu dengan AI

Panduan praktik Bootcamp Full-Stack Web Developer **harisenin.com** bersama **Adel Aulia**, IT Development Specialist di ARTOTEL Group.

Pada sesi ini, peserta membangun portfolio landing page menggunakan HTML, CSS, dan JavaScript dengan bantuan AI, lalu menguji dan mendokumentasikan hasilnya.

**Alur belajar:** Build → Test → Review → Portfolio.

> README ini merupakan panduan berdasarkan materi Day 2. Checklist di bawah adalah target praktik, bukan pernyataan bahwa proyek peserta sudah selesai atau lulus pengujian.

## Tujuan pembelajaran

Setelah mengikuti praktik, peserta diharapkan dapat:

- Membuat halaman portfolio responsif dengan tiga file sumber.
- Menggunakan AI untuk menghasilkan starter code dan membantu debugging.
- Menyesuaikan konten dengan identitas, keterampilan, dan pengalaman nyata.
- Memeriksa navigasi, tampilan mobile, aksesibilitas dasar, dan error browser.
- Menjelaskan proses pengerjaan melalui README, screenshot, dan cerita proyek.

## Hasil akhir

| Deliverable | Target |
| --- | --- |
| Kode | `index.html`, `style.css`, dan `script.js` |
| Halaman | Hero, About, Skills, tiga kartu proyek, dan Contact |
| Interaksi | Navigasi mobile yang dapat dibuka dan ditutup |
| Kualitas | Tampilan responsif, tautan berfungsi, dan review dasar |
| Dokumentasi | README proyek, screenshot, dan ringkasan proses pengerjaan |

Gunakan proyek yang benar-benar pernah dibuat. Jika masih berupa latihan atau rencana, jelaskan statusnya dengan jujur.

## Agenda kelas

| Waktu sesuai materi | Kegiatan |
| --- | --- |
| 19.05–19.25 | Project briefing, 20 menit |
| 19.25–20.25 | Guided hands-on, 60 menit |
| 20.25–20.45 | Mengubah hasil praktik menjadi materi portfolio, 20 menit |
| 20.45–20.55 | Tanya jawab, 10 menit |

## Tools dan persiapan

- Visual Studio Code sebagai editor.
- Browser untuk menjalankan halaman dan membuka Developer Tools.
- AI assistant melalui browser atau editor.
- Ekstensi Live Server, opsional.

Proyek menggunakan **HTML, CSS, dan vanilla JavaScript**, tanpa framework, external API, atau secret key. Tidak diperlukan instalasi package atau proses build.

1. Buat folder bernama `my-first-portfolio`.
2. Buka folder tersebut di Visual Studio Code.
3. Buat `index.html`, `style.css`, dan `script.js` dalam folder yang sama.
4. Buka AI assistant.
5. Atur browser dan editor berdampingan agar perubahan mudah diperiksa.

## Struktur file

| File | Fungsi |
| --- | --- |
| `index.html` | Struktur dan konten halaman menggunakan HTML semantik |
| `style.css` | Layout, warna, tipografi, dan penyesuaian tampilan mobile |
| `script.js` | Interaksi halaman, terutama menu navigasi mobile |
| `README.md` | Dokumentasi proyek setelah praktik |
| `screenshot.png` | Bukti tampilan hasil praktik setelah diambil peserta |

Tiga file pertama merupakan kode utama. README dan screenshot melengkapi dokumentasi.

## 1. Generate starter code

Salin prompt dari materi berikut ke AI assistant. Sesuaikan kebutuhan, lalu baca kode yang dihasilkan sebelum menggunakannya.

```text
Act as a patient frontend coding partner.
Create a beginner-friendly responsive
portfolio landing page using vanilla
HTML, CSS, JavaScript only.
Deliver exactly 3 files: index.html,
style.css, script.js. Sections: hero,
about, skills, 3 project cards, contact.
Include accessible navigation and
a working mobile menu. No frameworks,
external APIs, or secret keys.
Explain where each file belongs.
```

Simpan setiap hasil ke file yang sesuai. Jangan memasukkan penanda Markdown seperti ```html ke dalam file kode.

## 2. Hubungkan dan jalankan file

Pastikan `index.html` memuat stylesheet, viewport, dan script. Contoh berikut hanya menunjukkan kerangka penghubung file:

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Portfolio Saya</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js" defer></script>
  </head>
  <body>
    <main>
      <!-- Tambahkan konten portfolio di sini. -->
    </main>
  </body>
</html>
```

Untuk menjalankan halaman, buka `index.html` langsung di browser atau gunakan **Open with Live Server** jika ekstensi sudah terpasang. Simpan perubahan dan periksa kembali tampilan browser.

Jika CSS atau JavaScript tidak terbaca, periksa nama file, lokasi file, dan path pada `href` atau `src`. Buka DevTools Console untuk melihat pesan error.

## 3. Ikuti checkpoint praktik

| Menit | Aktivitas | Hal yang diperiksa |
| --- | --- | --- |
| 00–10 | Generate dan hubungkan tiga file | Halaman tampil, CSS dan JS termuat |
| 10–20 | Sesuaikan Hero, About, dan Skills | Konten sesuai profil peserta |
| 20–35 | Tambahkan kartu proyek dan kontak | Deskripsi faktual dan tautan bermakna |
| 35–45 | Perbaiki tampilan mobile | Konten terbaca tanpa overflow horizontal |
| 45–55 | Uji interaksi dan perbaiki bug | Menu dan navigasi bekerja |
| 55–60 | Simpan hasil dan screenshot | Catatan refleksi tersedia |

### Konten yang menunjukkan bukti

Jelaskan pekerjaan yang dilakukan secara konkret. Contoh berikut hanya boleh digunakan jika sesuai hasil praktik:

> Membuat landing page hotel responsif menggunakan HTML, CSS, dan JavaScript, lalu menguji tampilan mobile serta tautan navigasinya.

Lengkapi identitas, keterampilan, deskripsi proyek, dan kontak yang aman untuk dibagikan. Hapus placeholder sebelum publikasi.

### Interaksi menu mobile

Contoh berikut mengembangkan pola toggle pada slide dengan pengecekan kedua elemen:

```javascript
const menuBtn = document.querySelector('#menuBtn');
const nav = document.querySelector('#navLinks');

if (menuBtn && nav) {
  menuBtn.addEventListener('click', () => {
    const isOpen = nav.classList.toggle('open');
    menuBtn.setAttribute('aria-expanded', String(isOpen));
  });
}
```

Agar bekerja, HTML harus memiliki tombol dengan `id="menuBtn"` dan navigasi dengan `id="navLinks"`. Beri tombol `aria-controls="navLinks"` dan nilai awal `aria-expanded="false"` jika menu awalnya tertutup. CSS perlu mengatur tampilan navigasi pada layar kecil dan menampilkannya ketika kelas `.open` aktif.

Uji dengan klik langsung serta keyboard. Memasukkan kode saja belum membuktikan interaksi berfungsi.

## 4. Review dan debugging

Centang setiap poin setelah benar-benar diperiksa:

- [ ] Konten tidak memuat placeholder atau pencapaian yang dibuat-buat.
- [ ] Tombol, anchor, dan tautan kontak memiliki tujuan yang benar.
- [ ] Layout layar kecil tidak menimbulkan scroll horizontal.
- [ ] Menu mobile bisa dibuka dan ditutup.
- [ ] Gambar memiliki alt text yang sesuai.
- [ ] Heading tersusun logis dan fokus keyboard terlihat.
- [ ] Console tidak menampilkan error.
- [ ] Path CSS, JavaScript, dan gambar sudah benar.
- [ ] Tidak ada secret key atau informasi sensitif dalam file.

Saat meminta bantuan AI, jelaskan gejala, kondisi pengujian, kode terkait, dan pesan error. Contoh prompt dari materi:

```text
On mobile at 390px the menu stays hidden.
Here is the HTML, CSS, JS and console output.
Find the root cause and propose the smallest fix.

[Tempelkan kode terkait dan console output di sini.]
```

Setelah menerapkan perbaikan, ulangi pengujian yang sebelumnya gagal dan periksa apakah fungsi lain tetap bekerja.

### Fokus review instruktur

| Aspek | Bukti yang ditinjau |
| --- | --- |
| Hierarki visual | Judul, isi, dan tombol mudah dibaca |
| Responsivitas | Layout menyesuaikan ukuran layar |
| Fungsi | Tautan dan navigasi bekerja |
| Struktur dan aksesibilitas | HTML semantik serta navigasi yang dapat digunakan |
| Kejujuran konten | Deskripsi sesuai pekerjaan yang benar-benar dilakukan |

## 5. Jadikan proyek sebagai case study

Dokumentasikan empat hal berikut:

1. **Problem:** masalah yang ingin diselesaikan dan siapa pengguna halaman.
2. **Approach:** tools, keputusan desain, serta peran AI dalam pengerjaan.
3. **Evidence:** screenshot, kode, dan hasil pengujian yang benar-benar dilakukan.
4. **Learning:** kendala yang ditemukan dan cara memperbaikinya.

### Template README untuk proyek peserta

Salin template ini ke README milik proyek, lalu ganti semua bagian dalam tanda kurung siku:

```markdown
# My First Portfolio Landing Page

## Goal
[Jelaskan tujuan halaman dan siapa penggunanya.]

## Stack
HTML, CSS, vanilla JavaScript, dan [AI assistant yang digunakan].

## Features
[Tuliskan hanya fitur yang sudah dibuat dan berfungsi.]

## How to run
Buka index.html di browser atau gunakan Live Server.

## Screenshot
![Tampilan portfolio](screenshot.png)

## AI use and verification
- Bantuan AI: [prompt atau bagian kode yang dibantu AI].
- Perubahan pribadi: [konten, desain, atau kode yang diubah].
- Pengujian: [ukuran layar, navigasi, dan interaksi yang diuji].
- Perbaikan: [bug yang ditemukan dan tindakan perbaikannya].

## Learning
[Jelaskan pembelajaran utama dan hal yang masih perlu diperbaiki.]
```

Sertakan gambar `screenshot.png` dengan nama dan lokasi yang sesuai, atau sesuaikan path pada template.

## 6. Publikasi dan presentasi

Publikasi bersifat **opsional**, dilakukan setelah validasi:

1. Rapikan dan simpan tiga file sumber.
2. Tambahkan README proyek dan screenshot hasil aktual.
3. Masukkan proyek ke repository version control jika sudah siap.
4. Publikasikan melalui platform static hosting jika diinginkan.
5. Buka URL publik, lalu uji ulang tautan dan tampilan mobile.
6. Tulis ringkasan proyek yang jujur dalam 3–4 kalimat.

## Exit ticket

Sebelum mengakhiri sesi, jawab:

1. Apa yang kamu bangun?
2. Bagian mana yang dibantu oleh AI?
3. Apa yang kamu uji atau perbaiki sendiri?

---

Disusun berdasarkan materi **Harisenin BooKil Day 2 — Hands On: Project Pertamamu dengan AI**, Adel Aulia. Contoh penghubung file, pengecekan elemen JavaScript, dan petunjuk penggunaan diperjelas untuk membantu praktik mandiri.
