# Latihan Soal 1 Konversi Sistem Bilangan

## Tabel Ringkasan Hasil Konversi

| No | Soal Awal | Desimal (10) | Biner (2) | Oktal (8) | Heksadesimal (16) | BCD | Kode Gray |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **(a)** | 324 (Des) | 324 | 101000100 | 504 | 144 | 0011 0010 0100 | 111100110 |
| **(b)** | 115 (Des) | 115 | 1110011 | 163 | 73 | 0001 0001 0101 | 1001010 |
| **(c)** | 11010011 (Bin) | 211 | 11010011 | 323 | D3 | 0010 0001 0001 | 10111010 |
| **(d)** | 10011110 (Bin) | 158 | 10011110 | 236 | 9E | 0001 0101 1000 | 11010001 |
| **(e)** | 2AF (Heks) | 687 | 1010101111 | 1257 | 2AF | 0110 1000 0111 | 1111111000 |
| **(f)** | 1F9 (Heks) | 505 | 111111001 | 771 | 1F9 | 0101 0000 0101 | 100000101 |

---

## Tabel Referensi Tambahan

### 1. Tabel Kebenaran XOR (Untuk Kode Gray)
Operasi XOR menghasilkan nilai `1` jika kedua input **berbeda**, dan `0` jika kedua input **sama**.

| Input 1 | Input 2 | Hasil (XOR) |
| :---: | :---: | :---: |
| 0 | 0 | **0** |
| 0 | 1 | **1** |
| 1 | 0 | **1** |
| 1 | 1 | **0** |

### 2. Nilai Huruf Heksadesimal
| Heksadesimal | Nilai Desimal | Biner (4-bit) |
| :---: | :---: | :---: |
| **A** | 10 | 1010 |
| **B** | 11 | 1011 |
| **C** | 12 | 1100 |
| **D** | 13 | 1101 |
| **E** | 14 | 1110 |
| **F** | 15 | 1111 |

---

## Aturan Dasar Konversi

1. **Ke Desimal:** Kalikan setiap digit dengan basis asalnya pangkat posisi digit (dimulai dari 0 dari paling kanan).
2. **Ke Biner:** - Dari Desimal: Bagi bilangan dengan 2 secara berulang hingga habis, catat sisa baginya dari bawah ke atas.
   - Dari Heksadesimal/Oktal: Ubah setiap digit ke dalam 4-bit (untuk heksa) atau 3-bit (untuk oktal) biner.
3. **Ke Oktal & Heksadesimal (dari Biner):** - Oktal: Kelompokkan biner menjadi 3 bit dari kanan ke kiri, lalu ubah ke desimal (0-7).
   - Heksadesimal: Kelompokkan biner menjadi 4 bit dari kanan ke kiri, ubah ke desimal (0-15).
4. **Ke BCD:** Ubah setiap **satu digit angka desimal** langsung menjadi **4 bit biner**.
5. **Ke Kode Gray (dari Biner):**
   - Bit pertama (paling kiri/MSB) disalin langsung.
   - Bit berikutnya adalah hasil operasi XOR antara bit biner saat ini dengan bit biner di sebelah kirinya.

---

## Penjabaran Langkah-Langkah

### (a) Konversi 324 (Desimal)

* **Desimal:** 324
* **Biner:** 
  - 324 / 2 = 162 sisa 0
  - 162 / 2 = 81 sisa 0
  - 81 / 2 = 40 sisa 1
  - 40 / 2 = 20 sisa 0
  - 20 / 2 = 10 sisa 0
  - 10 / 2 = 5 sisa 0
  - 5 / 2 = 2 sisa 1
  - 2 / 2 = 1 sisa 0
  - 1 / 2 = 0 sisa 1
  - **Hasil:** 101000100
* **Oktal:** Kelompokkan biner (101)(000)(100) -> 5 0 4 -> **504**
* **Heksadesimal:** Kelompokkan biner (0001)(0100)(0100) -> 1 4 4 -> **144**
* **BCD:** 3(0011) 2(0010) 4(0100) -> **0011 0010 0100**
* **Kode Gray:** Dari biner 101000100
  - 1 (tetap)
  - 1 XOR 0 = 1
  - 0 XOR 1 = 1
  - 1 XOR 0 = 1
  - 0 XOR 0 = 0
  - 0 XOR 0 = 0
  - 0 XOR 1 = 1
  - 1 XOR 0 = 1
  - 0 XOR 0 = 0
  - **Hasil:** 111100110

---

### (b) Konversi 115 (Desimal)

* **Desimal:** 115
* **Biner:**
  - 115 / 2 = 57 sisa 1
  - 57 / 2 = 28 sisa 1
  - 28 / 2 = 14 sisa 0
  - 14 / 2 = 7 sisa 0
  - 7 / 2 = 3 sisa 1
  - 3 / 2 = 1 sisa 1
  - 1 / 2 = 0 sisa 1
  - **Hasil:** 1110011
* **Oktal:** (001)(110)(011) -> 1 6 3 -> **163**
* **Heksadesimal:** (0111)(0011) -> 7 3 -> **73**
* **BCD:** 1(0001) 1(0001) 5(0101) -> **0001 0001 0101**
* **Kode Gray:** Dari biner 1110011
  - Bit 1: 1 (tetap)
  - Bit 2: 1 XOR 1 = 0
  - Bit 3: 1 XOR 1 = 0
  - Bit 4: 1 XOR 0 = 1
  - Bit 5: 0 XOR 0 = 0
  - Bit 6: 0 XOR 1 = 1
  - Bit 7: 1 XOR 1 = 0
  - **Hasil Akhir:** 1001010

---

### (c) Konversi 11010011 (Biner)

* **Biner:** 11010011
* **Desimal:** (1 x 128) + (1 x 64) + (0 x 32) + (1 x 16) + (0 x 8) + (0 x 4) + (1 x 2) + (1 x 1) = 128 + 64 + 16 + 2 + 1 = **211**
* **Oktal:** (011)(010)(011) -> 3 2 3 -> **323**
* **Heksadesimal:** (1101)(0011) -> D 3 -> **D3**
* **BCD:** Menggunakan angka desimal (211) -> 2(0010) 1(0001) 1(0001) -> **0010 0001 0001**
* **Kode Gray:** Dari biner 11010011
  - 1 (tetap), 1^1=0, 1^0=1, 0^1=1, 1^0=1, 0^0=0, 0^1=1, 1^1=0
  - **Hasil:** 10111010

---

### (d) Konversi 10011110 (Biner)

* **Biner:** 10011110
* **Desimal:** (1 x 128) + (0 x 64) + (0 x 32) + (1 x 16) + (1 x 8) + (1 x 4) + (1 x 2) + (0 x 1) = 128 + 16 + 8 + 4 + 2 = **158**
* **Oktal:** (010)(011)(110) -> 2 3 6 -> **236**
* **Heksadesimal:** (1001)(1110) -> 9 E -> **9E**
* **BCD:** Dari desimal (158) -> 1(0001) 5(0101) 8(1000) -> **0001 0101 1000**
* **Kode Gray:** Dari biner 10011110
  - 1 (tetap), 1^0=1, 0^0=0, 0^1=1, 1^1=0, 1^1=0, 1^1=0, 1^0=1
  - **Hasil:** 11010001

---

### (e) Konversi 2AF (Heksadesimal)

* **Heksadesimal:** 2AF
* **Biner:** 2(0010) A(1010) F(1111) -> **1010101111**
* **Desimal:** (2 x 256) + (10 x 16) + (15 x 1) = 512 + 160 + 15 = **687**
* **Oktal:** Dari biner (001)(010)(101)(111) -> 1 2 5 7 -> **1257**
* **BCD:** Dari desimal (687) -> 6(0110) 8(1000) 7(0111) -> **0110 1000 0111**
* **Kode Gray:** Dari biner 1010101111
  - 1 (tetap), 1^0=1, 0^1=1, 1^0=1, 0^1=1, 1^0=1, 0^1=1, 1^1=0, 1^1=0, 1^1=0
  - **Hasil:** 1111111000

---

### (f) Konversi 1F9 (Heksadesimal)

* **Heksadesimal:** 1F9
* **Biner:** 1(0001) F(1111) 9(1001) -> **111111001**
* **Desimal:** (1 x 256) + (15 x 16) + (9 x 1) = 256 + 240 + 9 = **505**
* **Oktal:** Dari biner (111)(111)(001) -> 7 7 1 -> **771**
* **BCD:** Dari desimal (505) -> 5(0101) 0(0000) 5(0101) -> **0101 0000 0101**
* **Kode Gray:** Dari biner 111111001
  - 1 (tetap), 1^1=0, 1^1=0, 1^1=0, 1^1=0, 1^1=0, 1^0=1, 0^0=0, 0^1=1
  - **Hasil:** 100000101