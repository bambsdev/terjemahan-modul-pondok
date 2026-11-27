# AGENTS.md — Panduan Resmi Terjemahan Modul Pondok
> File ini adalah **acuan utama** bagi semua AI Agent yang mengerjakan proyek terjemahan modul pondok.
> Baca seluruh isi file ini sebelum memulai pekerjaan apapun.

---

## 1. GAMBARAN UMUM PROYEK

Proyek ini adalah penerjemahan kurikulum resmi Arab Saudi ke dalam Bahasa Indonesia agar dapat dipahami oleh murid-murid di lingkungan pondok pesantren.

| Item | Detail |
|---|---|
| **Sumber** | Kurikulum resmi Kerajaan Arab Saudi (Universitas Imam Muhammad bin Saud) |
| **Target Pembaca** | Murid kelas 7, 8, dan 9 (usia 13–15 tahun) |
| **Bahasa Terjemahan** | Bahasa Indonesia yang mudah, ringan, dan sesuai usia remaja |
| **Akun Google** | `ibrohimsairony@gmail.com` |
| **GitHub Username** | `bambsdev` |
| **GitHub Repo** | `terjemahan-modul-pondok` |

---

## 2. STRUKTUR FOLDER PROYEK

```
d:\proyek terjemahan modul pondok\
├── AGENTS.md                          ← file ini
├── fikih kelas 8 semester 1\
│   ├── master.pdf                     ← PDF sumber utama
│   ├── gambar\                        ← halaman_001.jpg s.d. halaman_053.jpg
│   ├── gambar_bagan_asli\             ← (dibuat agent) hasil crop bagan asli
│   ├── gambar_bagan_indonesia\        ← (dibuat agent) bagan versi Bahasa Indonesia
│   └── output\                        ← (dibuat agent) file markdown hasil terjemahan
├── fikih kelas 9 semester 1\
│   ├── master.pdf
│   ├── gambar\
│   ├── gambar_bagan_asli\
│   ├── gambar_bagan_indonesia\
│   └── output\
├── siroh kelas 7 semester 1\
│   ├── master.pdf
│   ├── gambar\
│   ├── gambar_ilustrasi_asli\         ← (dibuat agent) hasil crop ilustrasi asli
│   └── output\
├── siroh kelas 8 semester 1\
│   └── [sama dengan siroh 7]
└── siroh kelas 9 semester 1\
    └── [sama dengan siroh 7]
```

---

## 3. URUTAN PENGERJAAN

Kerjakan modul **Fikih terlebih dahulu**, lalu Siroh, mengikuti urutan kelas:

1. ✅ **Fikih kelas 8 semester 1** ← PILOT — wajib tunggu review Ustadz sebelum lanjut
2. ⏳ Fikih kelas 9 semester 1
3. ⏳ Siroh kelas 7 semester 1
4. ⏳ Siroh kelas 8 semester 1
5. ⏳ Siroh kelas 9 semester 1

> **PENTING:** Setelah selesai modul pertama (Fikih kelas 8), **HENTIKAN** dan tunggu review Ustadz. Jangan lanjut ke modul berikutnya tanpa persetujuan.

---

## 4. ATURAN BAHASA & TERJEMAHAN

### 4.1 Prinsip Umum
- Gunakan bahasa Indonesia yang **sederhana, ringan, dan mudah dipahami** oleh remaja usia 13–15 tahun.
- **JANGAN** gunakan kata-kata yang terlalu akademis, formal tinggi, atau jarang dipakai remaja Indonesia.
- **JANGAN** menambahkan materi, penjelasan, atau informasi yang **tidak ada** di `master.pdf`. Terjemahan harus otentik sesuai aslinya.

### 4.2 Istilah Arab
- Istilah-istilah Arab yang umum di pesantren (seperti: *Fardhu, Sunnah, Makruh, Mubah, Haram, Wajib, Matan, Syarah, Raka'at, Thaharah, Najis,* dll.) **tetap ditulis dalam bahasa Arab** apa adanya.
- **TIDAK PERLU** memberikan penjelasan dalam tanda kurung untuk istilah-istilah tersebut.

### 4.3 Ayat Al-Qur'an & Hadits
- **WAJIB** dicantumkan. Jangan pernah dihapus atau diringkas.
- Tulis teks Arab-nya secara utuh di **baris tersendiri** (karena Right-to-Left).
- Sertakan sumber rujukan (nama surah + nomor ayat, atau nama kitab hadits + nomor/perawi sesuai aslinya).
- Sertakan **terjemahan Bahasa Indonesia** tepat di bawah sumber rujukan agar mudah dipahami murid.
- Format contoh:

```
﴿ لَقَدْ كَانَ لَكُمْ فِي رَسُولِ اللَّهِ أُسْوَةٌ حَسَنَةٌ ﴾
(QS. Al-Ahzab: 21)
*"Sungguh, telah ada pada (diri) Rasulullah itu suri teladan yang baik bagimu."*

«مَنْ يُرِدِ اللَّهُ بِهِ خَيْرًا يُفَقِّهْهُ فِي الدِّينِ»
(HR. Bukhari: 71, Muslim: 1037)
*"Barang siapa yang Allah kehendaki kebaikan baginya, maka Allah akan memahamkannya dalam urusan agama."*
```

---

## 5. FORMAT TERJEMAHAN — FIKIH

### 5.1 Halaman yang Dilewati (SKIP)
Halaman-halaman berikut **jangan diterjemahkan** dan **tidak dimasukkan** ke Google Docs:
- Halaman sampul / cover
- Halaman hak cipta
- Halaman mukaddimah / pendahuluan / kata pengantar
- Halaman biografi penulis
- Halaman daftar isi
- Halaman jadwal mingguan / distribusi materi

> Halaman pertama Google Docs langsung dimulai dari **Bab/Pasal pertama** isi pelajaran.

### 5.2 Urutan Konten Per Bab (Fikih)

```
# Judul Bab **(1)**

[INTISARI PEMBAHASAN — 2–4 kalimat ramah remaja, tanpa label]

### Matan
[Terjemahan isi bab — Matan, dengan penanda **(1)**, **(2)**, dst.]

---

### Catatan Kaki
[Terjemahan seluruh Syarah / footnote bernomor **(1)**, **(2)**, dst.]

[Bagan Bahasa Indonesia jika ada]
[Pertanyaan (As-ilah) jika ada]
```

### 5.3 Intisari Pembahasan
- Ditulis sebagai **paragraf pendek** (2–4 kalimat) sebagai pengantar bab.
- Gunakan bahasa yang ramah remaja dan memotivasi.
- **AI yang generate sendiri** berdasarkan isi bab yang akan diterjemahkan.
- Jangan cantumkan label "Intisari Pembahasan" atau "Halaman sekian". Langsung tuliskan paragrafnya.
- Contoh format:

> *Pada bagian ini kita akan belajar tentang sujud sahwi, yaitu sujud yang dilakukan ketika kita lupa atau salah dalam sholat. Memahami ini penting agar sholat kita tetap sah dan sesuai tuntunan.*

### 5.4 Matan vs Catatan Kaki (Syarah)
- **Matan** (teks utama kitab) → diterjemahkan di bagian atas di bawah label **`Matan`**.
- **Catatan Kaki** (Syarah/penjelasan/komentar) → diterjemahkan di bagian bawah di bawah label **`Catatan Kaki`**.
- Keduanya **dipisahkan dengan garis horizontal (`---`)** dan label eksplisit **"Matan"** & **"Catatan Kaki"**.
- Khusus Fikih saja. Siroh tidak memiliki pemisah ini.

### 5.5 Footnote / Catatan Kaki
- **Wajib dimasukkan** seluruhnya ke dalam hasil terjemahan tanpa diringkas.
- Gunakan format **angka dalam kurung tebal** (`**(1)**`, `**(2)**`, dst.), baik di dalam teks Matan maupun di daftar Catatan Kaki.
- Terjemahkan isi footnote menggunakan bahasa yang tetap ringan dan mudah dipahami remaja usia 13–15 tahun.

### 5.6 Bagan / Diagram di Fikih
Jika ada bagan/diagram dalam bahasa Arab:

**Langkah wajib:**
1. **Crop** gambar bagan asli dari halaman JPG → simpan ke folder `gambar_bagan_asli\` dengan nama `bagan_hal_XXX.jpg`.
2. **Generate gambar baru** bagan yang sama tapi seluruh teksnya sudah diterjemahkan ke Bahasa Indonesia → simpan ke `gambar_bagan_indonesia\` dengan nama `bagan_hal_XXX_id.jpg`.
3. **Tempel** gambar bagan Bahasa Indonesia ke Google Docs pada posisi yang sesuai.
4. Gambar bagan asli di `gambar_bagan_asli\` disimpan sebagai arsip, **tidak** dimasukkan ke Google Docs.

### 5.7 Pertanyaan (As-ilah)
- Bagian pertanyaan **wajib ada** dan harus diteliti akurasinya dengan cermat.
- Pastikan terjemahan pertanyaan tidak mengubah makna atau maksud soal aslinya.
- Format: gunakan daftar bernomor (`ol`) agar rapi.

### 5.8 Format Teks (Umum Fikih)
- Boleh menggunakan `ul` (bullet) atau `ol` (nomor) untuk memudahkan pemahaman.
- Gunakan **teks tebal** untuk istilah-istilah penting.
- Ayat dan hadits di baris tersendiri (lihat 4.3).

---

## 6. FORMAT TERJEMAHAN — SIROH

### 6.1 Halaman yang Dilewati (SKIP)
Sama seperti Fikih (lihat 5.1), ditambah:
- Tabel jadwal mingguan / tabel distribusi topik mingguan → **hapus/skip seluruhnya**.

### 6.2 Format Konten Per Bab (Siroh)
- **Tidak ada** Intisari Pembahasan.
- **Tidak ada** pemisah Matan–Syarah (Siroh tidak memiliki struktur ini).
- Langsung tuliskan hasil terjemahan.
- Boleh gunakan `ul` / `ol` untuk memudahkan pemahaman.

### 6.3 Ilustrasi di Siroh
- Ilustrasi (gambar, foto, peta, dsb.) **jangan diubah** dan **jangan ditranslasikan**.
- Harus tetap sama persis seperti aslinya.
- **Langkah wajib:** Crop gambar ilustrasi dari halaman JPG → simpan ke `gambar_ilustrasi_asli\` dengan nama `ilustrasi_hal_XXX.jpg`.
- Tempel ilustrasi asli tersebut ke Google Docs pada posisi yang sesuai.

### 6.4 Pertanyaan (As-ilah) di Siroh
- Sama seperti Fikih — wajib ada, diteliti akurasinya, format nomor (`ol`).

---

## 7. OUTPUT — GOOGLE DOCS

### 7.1 Ketentuan Umum
- **Satu Google Docs per modul** (5 dokumen total).
- Dibuat menggunakan akun Google: `ibrohimsairony@gmail.com`.
- Nama dokumen mengikuti format: `[Nama Modul] - Terjemahan Indonesia`
  - Contoh: `Fikih Kelas 8 Semester 1 - Terjemahan Indonesia`

### 7.2 Struktur Dokumen
- Setiap Bab baru dimulai di halaman baru.
- Judul Bab menggunakan **Heading 1**.
- Sub-judul (pasal/fasal) menggunakan **Heading 2**.
- Teks isi menggunakan **Normal/Body Text**.
- Ayat/Hadits: rata kanan (right-align), teks Arab, baris tersendiri.
- Garis pemisah Matan–Syarah: menggunakan *Horizontal Line* di Google Docs.

### 7.3 Penyisipan Gambar
- Gambar bagan Bahasa Indonesia (Fikih) disisipkan tepat pada posisi yang sesuai dengan konteks teks.
- Ilustrasi asli (Siroh) disisipkan tepat pada posisi aslinya.

---

## 8. GITHUB WORKFLOW

### 8.1 Setup Awal (Hanya Sekali)
```bash
# Buat repo baru di GitHub
gh repo create bambsdev/terjemahan-modul-pondok --public --description "Terjemahan modul kurikulum Saudi untuk pondok pesantren"

# Clone ke lokal
git clone https://github.com/bambsdev/terjemahan-modul-pondok.git
```

### 8.2 Branch per Modul
Gunakan branch terpisah untuk setiap modul:

| Modul | Branch |
|---|---|
| Fikih kelas 8 semester 1 | `fikih-kelas-8-sem1` |
| Fikih kelas 9 semester 1 | `fikih-kelas-9-sem1` |
| Siroh kelas 7 semester 1 | `siroh-kelas-7-sem1` |
| Siroh kelas 8 semester 1 | `siroh-kelas-8-sem1` |
| Siroh kelas 9 semester 1 | `siroh-kelas-9-sem1` |

### 8.3 Yang Disimpan di GitHub
- File markdown hasil terjemahan (di folder `output\`)
- File gambar bagan Bahasa Indonesia (`gambar_bagan_indonesia\`)
- File gambar ilustrasi asli yang sudah di-crop (`gambar_ilustrasi_asli\`)
- File `AGENTS.md` ini (di root)

> **JANGAN** push file `master.pdf` atau folder `gambar\` (terlalu besar).

### 8.4 Aturan Push
- **Setiap selesai mengerjakan satu bab/pasal** → langsung push tanpa perlu izin.
- **Jangan tunggu** sampai satu modul selesai semua. Push per bab agar revisi tercatat.
- Format commit message:

```
[fikih-8] Terjemahan Bab: Sujud Sahwi
[siroh-7] Terjemahan Bab: Kehidupan Arab Pra-Islam
[fix] Perbaikan terjemahan Bab Thaharah
```

### 8.5 Push Command
```bash
git add .
git commit -m "[nama-modul] Terjemahan: [nama bab yang selesai]"
git push origin [nama-branch]
```

---

## 9. ALUR KERJA LENGKAP PER MODUL

```
1. Buka folder modul (contoh: fikih kelas 8 semester 1\)
2. Baca master.pdf DAN lihat file gambar\halaman_XXX.jpg untuk tiap halaman
3. Identifikasi halaman mana yang masuk kategori SKIP (mukaddimah, sampul, dll.)
4. Mulai dari halaman PERTAMA yang bukan SKIP
5. Untuk setiap bab:
   a. Generate Intisari Pembahasan (khusus Fikih)
   b. Terjemahkan Matan
   c. Terjemahkan Syarah
   d. Terjemahkan dan masukkan Footnote
   e. Jika ada bagan → crop asli, generate versi Indonesia
   f. Jika ada As-ilah → terjemahkan dengan cermat
   g. Simpan ke file markdown di output\
   h. Push ke GitHub
6. Setelah satu bab selesai di Google Docs → masukkan konten ke Google Docs
7. Setelah seluruh modul selesai → lapor ke user untuk review Ustadz
8. TUNGGU approval sebelum lanjut modul berikutnya (khusus modul pilot: Fikih kelas 8)
```

---

## 10. CHECKLIST KUALITAS

Sebelum push ke GitHub dan submit ke Google Docs, pastikan:

- [ ] Tidak ada halaman mukaddimah/pendahuluan/sampul yang masuk
- [ ] Ayat Al-Qur'an dan hadits: teks Arab utuh ada, sumber rujukan ada, baris terpisah
- [ ] Istilah Arab pesantren tidak diterjemahkan paksa
- [ ] Bahasa Indonesia mudah dipahami remaja 13–15 tahun
- [ ] Intisari Pembahasan ada di awal setiap bab (Fikih)
- [ ] Pemisah Matan–Syarah ada (`---`) (Fikih)
- [ ] Footnote sudah diterjemahkan dan dimasukkan
- [ ] Bagan asli sudah di-crop dan disimpan di `gambar_bagan_asli\`
- [ ] Bagan versi Indonesia sudah dibuat dan disisipkan di Google Docs
- [ ] Pertanyaan (As-ilah) sudah diteliti akurasinya
- [ ] Tabel jadwal mingguan (Siroh) sudah dihapus/skip
- [ ] Tidak ada materi tambahan dari luar modul asli
- [ ] Commit dan push sudah dilakukan

---

## 11. CATATAN TEKNIS TAMBAHAN

### 11.1 Membaca Halaman
- Gunakan file `gambar\halaman_XXX.jpg` sebagai referensi visual utama.
- `master.pdf` sebagai referensi sekunder jika gambar kurang jelas.
- Untuk halaman yang teksnya berdempetan atau sulit dibaca, andalkan kedua sumber tersebut.

### 11.2 Footnote / Catatan Kaki di Fikih
- Footnote biasanya ada di bagian bawah halaman, dipisah garis tipis, dengan nomor dalam kurung (`(١)`, `(٢)`, dst.) yang berisi Syarah kitab.
- Meskipun teknis, tetap terjemahkan dengan bahasa yang ringan dan mudah.
- Gunakan format kurung tebal (`**(1)**`, `**(2)**`, dst.).
- Jika satu bagian Matan (Bab atau Fasal) bersambung lintas beberapa halaman, penomoran catatan kaki dibuat **menyambung berurutan** di dalam satu bagian tersebut (misal `**(1)**`–`**(25)**`) agar teks Matan tetap utuh dan tidak ada nomor catatan kaki yang ganda, lalu di-reset kembali ke `**(1)**` pada Fasal/Bab berikutnya.

### 11.3 Halaman yang Meragukan
- Jika ragu apakah halaman termasuk SKIP atau tidak → **masukkan saja** (lebih aman).
- Jika ragu terjemahan suatu kalimat → pilih padanan yang paling natural di telinga remaja Indonesia.

### 11.4 Google Docs API
- Gunakan plugin Google Docs (`gdocs`) yang sudah terkoneksi dengan `ibrohimsairony@gmail.com`.
- Jangan buat dokumen baru setiap sesi — cek dulu apakah dokumen untuk modul tersebut sudah ada.
- Simpan Document ID di file `output\doc_id.txt` agar bisa dilanjutkan sesi berikutnya.

---

*AGENTS.md ini dibuat pada 2026-11-26. Diperbarui sesuai kebutuhan.*
