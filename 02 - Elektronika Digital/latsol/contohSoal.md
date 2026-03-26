# Contoh Soal Konversi Sistem Bilangan

## Daftar Isi
1. [Konversi Oktal ke Desimal](#1-oktal-ke-desimal)
2. [Konversi Heksadesimal ke Desimal](#2-heksadesimal-ke-desimal)
3. [Konversi Biner ke Desimal](#3-biner-ke-desimal)
4. [Konversi Biner ke Oktal](#4-biner-ke-oktal)
5. [Konversi Desimal ke Biner](#5-desimal-ke-biner)
6. [Penjumlahan Biner](#6-penjumlahan-biner)
7. [Konversi Desimal ke Oktal](#7-desimal-ke-oktal)
8. [Konversi BCD ke Desimal](#8-bcd-ke-desimal)
9. [Konversi Gray Code ke Biner](#9-gray-code-ke-biner)
10. [Konversi Biner ke Gray Code](#10-biner-ke-gray-code)

---

### 1. Oktal ke Desimal
**Soal:** Ubah $261_{8}$ ke desimal.
**Langkah-langkah:**
* $(2 \times 8^2) + (6 \times 8^1) + (1 \times 8^0)$
* $128 + 48 + 1 = 177_{10}$
**» Hasil Akhir:** `177`

### 2. Heksadesimal ke Desimal
**Soal:** Ubah $F0_{16}$ ke desimal.
**Langkah-langkah:**
* $(15 \times 16^1) + (0 \times 16^0)$
* $240 + 0 = 240_{10}$
**» Hasil Akhir:** `240`

### 3. Biner ke Desimal
**Soal:** Ubah $10011110_{2}$ ke desimal.
**Langkah-langkah:**
* $2^7 + 2^4 + 2^3 + 2^2 + 2^1$
* $128 + 16 + 8 + 4 + 2 = 158_{10}$
**» Hasil Akhir:** `158`

### 4. Biner ke Oktal
**Soal:** Ubah $110100_{2}$ ke oktal.
**Langkah-langkah:**
Pecah biner menjadi kelompok 3-bit dari kanan:
* `110` = 6
* `100` = 4
**» Hasil Akhir:** `64`

### 5. Desimal ke Biner
**Soal:** Ubah $192_{10}$ ke biner.
**Langkah-langkah:**
* $192 - 128 (2^7) = 64$
* $64 - 64 (2^6) = 0$
**» Hasil Akhir:** `11000000`

### 6. Penjumlahan Biner
**Soal:** Tambahkan $22_{10}$ dan $7_{10}$ menggunakan penjumlahan biner.
**Langkah-langkah:**
1.  **Konversi:** $22_{10} = 10110_2$ dan $7_{10} = 00111_2$
2.  **Proses Penjumlahan:**
    ```text
      (Carry)  1 1 1 1
               1 0 1 1 0  (22)
             + 0 0 1 1 1  (7)
             -----------
               1 1 1 0 1  (Hasil: 29)
    ```
**» Hasil Akhir:** `11101`

### 7. Desimal ke Oktal
**Soal:** Ubah $189_{10}$ ke oktal.
**Langkah-langkah:**
* $189 \div 8 = 23$ (Sisa 5)
* $23 \div 8 = 2$ (Sisa 7)
* $2 \div 8 = 0$ (Sisa 2)
**» Hasil Akhir:** `275`

### 8. BCD ke Desimal
**Soal:** Ubah $0110000001111001$ (BCD) ke desimal.
**Langkah-langkah:**
Pisahkan setiap 4-bit (nibel):
* `0110` = 6 | `0000` = 0 | `0111` = 7 | `1001` = 9
**» Hasil Akhir:** `6079`

### 9. Gray Code ke Biner
**Soal:** Ubah $1011001011$ (Gray) ke biner.
**Langkah-langkah:**
* Bit 1: 1
* Bit 2: $1 \oplus 0 = 1$
* Bit 3: $1 \oplus 1 = 0$
* Bit 4: $0 \oplus 1 = 1$
* Bit 5: $1 \oplus 0 = 1$
* Bit 6: $1 \oplus 0 = 1$
* Bit 7: $1 \oplus 1 = 0$
* Bit 8: $0 \oplus 0 = 0$
* Bit 9: $0 \oplus 1 = 1$
* Bit 10: $1 \oplus 1 = 0$
**» Hasil Akhir:** `1101110010`

### 10. Biner ke Gray Code
**Soal:** Ubah $1101110010$ (Biner) ke gray.
**Langkah-langkah:**
* Bit 1: 1
* Bit 2: $1 \oplus 1 = 0$
* Bit 3: $1 \oplus 0 = 1$
* Bit 4: $0 \oplus 1 = 1$
* Bit 5: $1 \oplus 1 = 0$
* Bit 6: $1 \oplus 1 = 0$
* Bit 7: $1 \oplus 0 = 1$
* Bit 8: $0 \oplus 0 = 0$
* Bit 9: $0 \oplus 1 = 1$
* Bit 10: $1 \oplus 0 = 1$
**» Hasil Akhir:** `1011001011`