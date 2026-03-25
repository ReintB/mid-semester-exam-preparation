# Elektronika Digital

## Daftar Isi
- [1. Sistem Bilangan (Number Systems)](#1-sistem-bilangan-number-systems)
- [2. Konversi Antar Bilangan](#2-konversi-antar-bilangan)
- [3. BCD (Binary-Coded Decimal)](#3-bcd-binary-coded-decimal)
- [4. Gray Code (Kode Gray)](#4-gray-code-kode-gray)
- [5. Satuan Data Komputasi digital (Nibble, Byte, Word)](#5-satuan-data-komputasi-digital-nibble-byte-word)
- [6. Alphanumeric Code & ASCII](#6-alphanumeric-code--ascii)
- [7. Aritmatika Biner (Binary Arithmetic)](#7-aritmatika-biner-binary-arithmetic)

---

## 1. Sistem Bilangan (Number Systems)
**Definisi:** Sistem bilangan adalah metode matematika untuk merepresentasikan (mewakili) besaran dari sebuah kuantitas/objek fisik. Dalam sistem digital, semua sinyal logika komputer pada dasarnya diukur menggunakan angka berbasis (radix).

### Jenis-Jenis Sistem Bilangan:
1. **Desimal (Basis 10):** Menggunakan 10 simbol angka (0, 1, 2, 3, 4, 5, 6, 7, 8, 9).
   - *Contoh:* $256_{10}$
2. **Biner (Basis 2):** Sistem dasar mesin/komputer yang hanya mengenal 2 simbol (0 dan 1). Nilai 0 berarti *Off/Low*, 1 berarti *On/High*.
   - *Contoh:* $1011_{2}$
3. **Oktal (Basis 8):** Menggunakan 8 simbol angka (0, 1, 2, 3, 4, 5, 6, 7). Sistem ini sering dipakai untuk merangkum biner agar lebih ringkas (1 digit oktal = 3 bit biner).
   - *Contoh:* $42_{8}$
4. **Heksadesimal (Basis 16):** Menggunakan 16 simbol (0-9, lalu A, B, C, D, E, F). A=10, B=11, C=12, D=13, E=14, F=15. Sering digunakan pada pengalamatan memori/mikrokontroler (1 digit heksa = 4 bit biner).
   - *Contoh:* $2F_{16}$

---

## 2. Konversi Antar Bilangan

> **Tips Mudah Konversi:** 
> - **Dari Desimal ke yang lain:** Selalu gunakan **Pembagian Berulang** dengan basis tujuannya, lalu tulis hasil sisanya (*remainder*) dari bawah ke atas.
> - **Dari yang lain ke Desimal:** Gunakan **Perkalian Bobot/Pangkat** (dikalikan dengan basisnya yang dipangkatkan urutan posisinya dari kanan, dimulai dari pangkat 0).
> - **Antara Biner ↔ Oktal / Heksadesimal:** Jangan lewat desimal! Gunakan metode **Pengelompokan Bit** (Oktal = 3 bit, Heksa = 4 bit).

### A. Desimal ke Biner (Pembagian 2)
**Tahapan:** Bagi angka desimal dengan 2. Catat sisa baginya (0 atau 1). Ulangi sampai hasil baginya nol. Susun sisa bagi dari proses terakhir ke pertama (bawah ke atas).
- **Contoh:** $13_{10} \rightarrow \dots_{2}$
  - $13 / 2 = 6$, sisa **1** (LSB / Bit paling kanan)
  - $6 / 2 = 3$, sisa **0**
  - $3 / 2 = 1$, sisa **1**
  - $1 / 2 = 0$, sisa **1** (MSB / Bit paling kiri)
  - **Hasil:** $1101_{2}$

### B. Biner ke Desimal (Perkalian Bobot)
**Tahapan:** Kalikan setiap bit biner dengan nilai tempatnya ($2^0, 2^1, 2^2$, dst dimulai dari paling kanan). Angka 0 abaikan, jumlahkan nilai yang bitnya 1.
- **Contoh:** $1011_{2} \rightarrow \dots_{10}$
  - $(1 \times 2^3) + (0 \times 2^2) + (1 \times 2^1) + (1 \times 2^0)$
  - $8 + 0 + 2 + 1 = 11$
  - **Hasil:** $11_{10}$

### C. Biner ↔ Oktal (Metode Kelompok 3-bit)
**Tahapan Biner ke Oktal:** Kelompokkan biner ukurannya per 3 bit dari arah paling kanan. Ubah tiap 3 bit tersebut menjadi 1 digit oktal.
- **Contoh:** $101110_{2} \rightarrow \dots_{8}$
  - Pisahkan: `101` dan `110`
  - Terjemahkan per kotak: `101` = 5, `110` = 6
  - **Hasil:** $56_{8}$

### D. Biner ↔ Heksadesimal (Metode Kelompok 4-bit)
**Tahapan Biner ke Heksa:** Kelompokkan biner ukurannya per 4 bit dari arah kanan.
- **Contoh:** $10110101_{2} \rightarrow \dots_{16}$
  - Pisahkan: `1011` dan `0101`
  - Terjemahkan: `1011` = 11 (yaitu B), `0101` = 5
  - **Hasil:** $B5_{16}$

---

## 3. BCD (Binary-Coded Decimal)
**Definisi:** BCD adalah sistem di mana *setiap digit dari angka desimal* direpresentasikan secara mandiri oleh 4-bit biner. Berbeda dengan konversi biner murni yang membagi keseluruhan nilai sekaligus. Nilai BCD tertinggi per kelompok 4-bit hanyalah 1001 (9). Kombinasi 1010-1111 (A-F) tidak valid/terlarang di BCD.

### A. Konversi Desimal ke BCD
**Cara:** Pisahkan setiap digit desimal, lalu ubah satuan ukur masing-masing digit itu menggunakan kode biner 4-bit.
- **Contoh:** $137_{10} \rightarrow \dots_{BCD}$
  - 1 = `0001`
  - 3 = `0011`
  - 7 = `0111`
  - **Hasil:** $0001 \ 0011 \ 0111_{BCD}$ (perhatikan bedanya dengan biner murni $137_{10} = 10001001_2$)

### B. Konversi BCD ke Desimal
**Cara:** Sama seperti dari biner ke heksa, kelompokkan menjadi blok 4-bit dari kanan ke kiri, lalu terjemahkan masing-masing blok 4-bit tersebut menjadi angka desimal tunggal 0-9.
- **Contoh:** $10000101_{BCD} \rightarrow \dots_{10}$
  - Pisah 4-bit: `1000` dan `0101`
  - Baca nilai: `1000` = 8, `0101` = 5
  - **Hasil:** $85_{10}$

---

## 4. Gray Code (Kode Gray)
**Definisi:** Gray Code adalah kode biner tak berbobot (*unweighted*) di mana nilai yang posisinya saling berurutan (misal dari representasi 3 ke 4) hanya memiliki **perbedaan tepat pada 1 bit saja**. Tujuannya amat krusial pada sensor posisi mekanis (seperti rotary encoder) untuk mencegah *error* transisi yang disebabkan fluktuasi saat banyak bit berubah serentak.

### A. Konversi Biner ke Gray Code
**Cara:** 
1. Bit paling kiri (MSB/Most Significant Bit) langsung diturunkan ke bawah, tidak berubah nilainya.
2. Untuk bit Gray berikutnya: Lakukan operasi kombinasi **XOR (Exclusive OR)** antara bit biner posisi sekarang dengan bit biner di posisi sebelah kirinya ($0 \oplus 0 = 0$; $1 \oplus 1 = 0$; $0 \oplus 1 = 1$; $1 \oplus 0 = 1$). 
   - *Intonasi Gampang: Kalau angka binernya **beda** hasil XOR 1, kalau **kembar** hasil XOR 0.*

**Visualisasi & Contoh:** Biner $1011_{2} \rightarrow \dots_{\text{Gray}}$
```text
Biner :   1         0         1         1
          |  \      |  \      |  \      |
          |   \     |   \     |   \     |
          |    > ⊕       > ⊕       > ⊕
          |      |         |         |
          V      V         V         V
Gray  :   1      1         1         0
```
- MSB (1) langsung turun menjadi 1.
- Lalu, biner 1 $\oplus$ biner 0 = 1.
- Lalu, biner 0 $\oplus$ biner 1 = 1.
- Lalu, biner 1 $\oplus$ biner 1 = 0.
- **Hasil Gray =** $1110$

### B. Konversi Gray Code ke Biner
**Cara:**
1. Bit paling kiri (MSB) tetap diturunkan langsung ke bawah.
2. Untuk bit Biner berikutnya: Lakukan silang **XOR** antara *bit Biner yang baru saja didapatkan di bawah*, dengan *bit Gray yang ada di posisi ketetanggaan selanjutnya di atas*.

**Visualisasi & Contoh:** Gray $1110 \rightarrow \dots_{2}$ (Biner)
```text
Gray  :   1         1         1         0
          |         |         |         |
          |   +--> ⊕    +--> ⊕    +--> ⊕
          |   |    |    |    |    |    |
          V   |    V    |    V    |    V
Biner :   1---+    0----+    1----+    1
```
*(Garis menyilang dari bawah ke atas melambangkan bit biner hasil sebelumnya ditarik miring untuk di-XOR-kan dengan bit Gray selanjutnya)*

- MSB (1) langsung turun menjadi 1.
- Lalu, biner 1 ditarik menyilang ke atas $\oplus$ gray 1 = 0.
- Lalu, biner 0 ditarik menyilang ke atas $\oplus$ gray 1 = 1.
- Lalu, biner 1 ditarik menyilang ke atas $\oplus$ gray 0 = 1.
- **Hasil Biner =** $1011_{2}$ 

---

## 5. Satuan Data Komputasi digital (Nibble, Byte, Word)
- **Bit (Binary Digit):** Elemen unit data terkecil dari informasi di komputer, nilainya murni hanya bernilai `0` atau `1`.
- **Nibble:** Kumpulan logika yang terdiri dari kombinasi tepat **4 bit**. Satu heksadesimal atau satu digit BCD murni menempati ukuran 1 nibble ini. (Contoh: `1011`).
- **Byte:** Kumpulan memori yang terdiri dari kumpulan kelipatan tepat **8 bit** (atau dapat dikatakan 2 buah Nibble sekaligus). Ini adalah representasi standar ukuran karakter tunggal terkecil di tempat penyimpanan PC modern. (Contoh: `11000101`).
- **Word:** Kumpulan bit yang ukurannya mempresentasikan besaran batasan lajur memori (data bus line) atau register internal pada satu siklus prosesor alat ukur tersebut. Biasanya pada perangkat keras moderen berukuran 16 bit, 32 bit, atau 64 bit (*sangat tergantung pada arsitektur sistem komputernya*).

---

## 6. Alphanumeric Code & ASCII
**Definisi:** Agar komputer tidak hanya menampilkan besaran hitungan matematika melainkan juga bisa untuk mengirim teks huruf (alphabet), tanda baca *punctuation*, elemen spasi, dan simbol grafis ke unit layar UI operator, diciptakanlah "Kode Alfanumerik". 

**ASCII (American Standard Code for Information Interchange):**
Adalah format sistem pengkodean alfanumerik bahasa inggris yang paling lazim digunakan global. Pada format awalnya adalah murni standar representasi kode **7-bit** (yang merepresentasikan 128 karakter bentuk yang berbeda). Saat ini seiring perkembangannya yang mana banyak dipakai meluas adalah modifikasi sistem per satu byte **8-bit** (dikenal meluas sebagai *Extended ASCII*) dengan daya tampung simpanan varian kompresi yang bisa membedakan hingga 256 karakter/simbol yang beda jenis spesifiknya sedari awal mula.  
- **Contoh ASCII yang sering muncul di ujian atau kuis:**
  - Huruf Besar (A) = Nilai desimal $65_{10}$ = Biner padanannya adalah $01000001_2$
  - Huruf Kecil (a) = Nilai desimal $97_{10}$ = Biner padanannya adalah $01100001_2$
  - Angka Karakter (0) = Nilai desimal $48_{10}$ = Biner padanannya adalah $00110000_2$

---

## 7. Aritmatika Biner (Binary Arithmetic)

### A. Penjumlahan Biner (Addition)
**Aturan Dasar Penjumlahan Logika Digital:**
- $0 + 0 = 0$
- $0 + 1 = 1$
- $1 + 0 = 1$
- $1 + 1 = 0$ dengan **Carry 1** (Artinya kita harus Meneruskan simpanan nilai 1 tersebut untuk dilempar ke penambahan di urutan bit kolom sebelah kirinya, layaknya pada matematika biasa di mana nilainya melebihi 9 di sistem normal desimal).
- $1 + 1 + 1$ (karena terdapat tumpukan sisa carry sebelumnnya) $= 1$ dengan status juga meneruskan sebuah **Carry 1**.

**Contoh Dasar:** $1010_2 + 0011_2$
```text
  1010
  0011
  ---- +
  1101
```

**Contoh Bersusun Kompleks dengan Nilai Carry:** $1011_2 + 1101_2$
```text
  111      <-- Carry Over dari penambahan bit kolom kanan
  1011 (Nilai 11 pada sistem desimal biasa)
  1101 (Nilai 13 pada sistem desimal biasa)
  ---- +
 11000 (Terjadi pergeseran melebar jadi 24 pada pembacaan desimal biasa)
```

### B. Pengurangan Biner (Subtraction)
**Aturan Dasar Pengurangan Logika Digital:**
- $0 - 0 = 0$
- $1 - 1 = 0$
- $1 - 0 = 1$
- $0 - 1 = 1$ dengan kewajiban memiliki status hutang **Borrow 1** (Tugasnya adalah meminjam nilai 1 dari tempat kolom bit di wilayah sebelah sebelah kirinya langsung). Pada saat meminjam nilai 1 mutlak dari tempat kiri persisnya tersebut, angka mutlak 1 tersebut turun drastis menempati perwakilan bobot "angka 2" buat peruntukan posisi asli yang sedang kesusahan meminjamnya (Logika ini seibarat kita kepepet meminjam di angka puluhan pada sistem standar pengurangan di kehidupan pengantar desimal kita lazim, tapi karena ini dasar dua maka jadinya nilai $2 - 1 = 1$).

**Contoh Kompleks Perhitungan Kasus Borrow:** $1010_2 \ (10) - 0101_2 \ (5)$
```text
  0 10 0 10    <-- Simulasi Status Keuangan Bayangan setelah siklus saling hutang Pinjam (Borrow Method)
  1  0 1  0    <-- Bilangan Atas (Yang Dikurangi)
  0  1 0  1    <-- Bilangan Tarikan Pengurang (Subtraktor)
  --------- -
  0  1 0  1    (Perolehan Sisa adalah Murni angka 5 di sistem desimal)
```
**Tahapan Urutannya supaya mudah dipahami:**
1. Peninjauan Kolom paling kanan: Angka $0$ dikurangi $1$ tentu tidak bisa. Karena itu dia terpaksa pinjam nilai solid 1 dari kolom kiri tetangganya, jadinya status barunya dia sekarang bernilai komputasi perolehan $2 - 1 = 1$.
2. Peninjauan Kolom kedua: Tadinya dia adalah angka dermawan tinggi memiliki jangkauan tegangan tinggi $1$, namun karena baru sja dipinjam temannya sehingga dia harus ikhlas nilai *on* itu habis jadi $0$. Maka sisa pertarungannya menantang bawah tinggal $0 - 0 = 0$.
3. Peninjauan Kolom ketiga: Angka sisa $0$ dikurangi $1$. Kasus Defisit Angka ini terjadi Kembali, maka dia pada bagian kolom penengah ketiga posisinya ini kini harus merengek meminjam lagi sebuah sumbangan angka 1 dari sebelahnya di arah kiri (dari digit mulia sang raja MSB di tepian yang posisinya berposisi paling kiri pucuk ujung penempatan bernilai tinggi $1$). Maka Sisa sumbangan hutang pinjaman tersebut bergejolak menjadi: konversi perolehan nilai taksiran pinjaman $(2) - 1 = 1$.
4. Peninjauan Kolom tersisa ujung keempat: Statusnya dia dulunya tadinya gagah perkasa $1$ tetapi sayang sekali nyawa nilainya telah ludes tak bersisa lantaran baru saja disedot sumbangannya dipinjam krisis yang kolom ketiga tadi, jadi terpaksa karena statusnya sekarang terjun sisa murni tak bertegangan di nilai matinya sang $0$, sisanya dieksekusi dengan mudah dalam keadaan pertarungan ringan $0 - 0 = 0$.
5. Hasil akhirnya dirangkai dan dikumpulkan jadi untaian string: Nilai output dari sirkuit terminal keluaran logikanya adalah `0101`

---
[<< 01 - Praktikum Teknologi Mekanik](../01%20-%20Praktikum%20Teknologi%20Mekanik/README.md) | [HOME](../README.md) | [03 - Praktikum Instrumentasi dan Pengukuran >>](../03%20-%20Praktikum%20Instrumentasi%20dan%20Pengukuran/README.md)