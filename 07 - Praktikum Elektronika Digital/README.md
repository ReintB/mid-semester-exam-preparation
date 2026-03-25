# Praktikum Elektronika Digital

## Daftar Isi
- [Modul 1: Gerbang Logika Dasar (AND, OR, NOT)](#modul-1-gerbang-logika-dasar-and-or-not)
- [Modul 2: Gerbang Logika Lanjutan (NAND, NOR, X-OR, X-NOR)](#modul-2-gerbang-logika-lanjutan-nand-nor-x-or-x-nor)
- [Modul 3-4: Rangkaian Paralel Adder (Penjumlah) & Subtractor](#modul-3-4-rangkaian-paralel-adder-penjumlah--subtractor)
- [Modul 5 & 6: Encoder dan Decoder](#modul-5--6-encoder-dan-decoder)
- [Modul 7 & 8: Multiplexer (MUX) & Demultiplexer (DEMUX)](#modul-7--8-multiplexer-mux--demultiplexer-demux)
- [Modul 9, 10, & 11: Rangkaian Flip-Flop](#modul-9-10--11-rangkaian-flip-flop)
- [Modul 12 & 13: Rangkaian Counter (Pencacah / Penghitung)](#modul-12--13-rangkaian-counter-pencacah--penghitung)

---

## Modul 1: Gerbang Logika Dasar (AND, OR, NOT)
Gerbang logika dasar adalah blok bangunan mutlak dari setiap sistem digital. Masing-masing mempunyai persamaan Boolean matematis, tabel kebenaran (*truth table*), dan nomor jenis IC standar tersendiri.

### 1. Gerbang AND (IC 7408)
- **Logika:** Mengeluarkan *Output High (1)* HANYA JIKA **Semua** *Input-nya High (1)*. Bisa diibaratkan seperti dua saklar yang dirangkai **Seri** (Lampu baru menyala jika saklar A dan saklar B ditutup bersamaan).
- **Persamaan Boolean:** $Y = A \cdot B$ (dibaca A *and* B)
- **Tabel Kebenaran (2 Input):**

  | Input A | Input B | Output Y |
  |:---:|:---:|:---:|
  | 0 | 0 | **0** |
  | 0 | 1 | **0** |
  | 1 | 0 | **0** |
  | 1 | 1 | **1** |
- **Varian IC lain:** IC 7411 (3-input AND), IC 7421 (4-input AND).

### 2. Gerbang OR (IC 7432)
- **Logika:** Mengeluarkan *Output High (1)* JIKA **Minimal ada Satu** saja dari *Input-nya High (1)*. Bisa diibaratkan seperti dua saklar yang dirangkai **Paralel** (Cukup salah satu saklar ditutup untuk menyalakan lampu).
- **Persamaan Boolean:** $Y = A + B$ (dibaca A *or* B)
- **Tabel Kebenaran (2 Input):**

  | Input A | Input B | Output Y |
  |:---:|:---:|:---:|
  | 0 | 0 | **0** |
  | 0 | 1 | **1** |
  | 1 | 0 | **1** |
  | 1 | 1 | **1** |

### 3. Gerbang NOT / Inverter (IC 7404)
- **Logika:** Membalikkan keadaan inputnya (Jika diberi 0 jadi 1, jika diberi 1 jadi 0). Hanya memiliki tepat 1 kaki input dan 1 kaki output per gerbangnya.
- **Persamaan Boolean:** $Y = \bar{A}$ (dibaca *A NOT* atau *A Bar*)
- **Tabel Kebenaran:**

  | Input A | Output Y |
  |:---:|:---:|
  | 0 | **1** |
  | 1 | **0** |

---

## Modul 2: Gerbang Logika Lanjutan (NAND, NOR, X-OR, X-NOR)
Gerbang-gerbang gabungan (Universal & Eksklusif) yang paling banyak dipakai pada logika-logika kontrol automasi.

### 1. Gerbang NAND (IC 7400)
- **Logika:** Gabungan dari NOT-AND. Outputnya **kebalikan dari tabel AND**. Ia menghasilkan output *Low (0)* hanya ketika semua inputnya *High (1)*. Ini sering disebut sebagai *Universal Gate* karena bisa dirangkai/dimanipulasi menjadi AND/OR/NOT murni.
- **Persamaan Boolean:** $Y = \overline{A \cdot B}$ 
- **Tabel Kebenaran (2 Input):**

  | Input A | Input B | Output Y (AND) | Output Y (NAND) |
  |:---:|:---:|:---:|:---:|
  | 0 | 0 | 0 | **1** |
  | 0 | 1 | 0 | **1** |
  | 1 | 0 | 0 | **1** |
  | 1 | 1 | 1 | **0** |
- **Varian IC lain:** IC 7410 (3-input NAND), IC 7420 (4-input NAND), IC 7430 (8-input NAND).

### 2. Gerbang NOR (IC 7402)
- **Logika:** Gabungan dari NOT-OR. Outputnya **kebalikan dari tabel OR**. Output akan *High (1)* hanya pada saat **Semua Input-nya Low (0)**. Juga merupakan gerbang universal. 
- **Persamaan Boolean:** $Y = \overline{A + B}$ 
- **Tabel Kebenaran (2 Input):**

  | Input A | Input B | Output Y (OR) | Output Y (NOR) |
  |:---:|:---:|:---:|:---:|
  | 0 | 0 | 0 | **1** |
  | 0 | 1 | 1 | **0** |
  | 1 | 0 | 1 | **0** |
  | 1 | 1 | 1 | **0** |
- **Varian IC lain:** IC 7427 (3-input NOR).

### 3. Gerbang EX-OR / Exclusive-OR (IC 7486)
- **Logika:** **Ganjil/Beda = 1**. Jika kedua input memiliki nilai logika yang **BERBEDA**, maka output = 1. Jika kembar/sama, output = 0. Sangat penting, dipakai untuk komponen konversi Gray code, Half-adder, Comparator.  *(Berbeda dengan OR biasa yang bernilai 1 jika keduanya 1)*.
- **Persamaan Boolean:** $Y = A \oplus B$ 
- **Tabel Kebenaran:**

  | Input A | Input B | Output Y (OR) | Output Y (X-OR) |
  |:---:|:---:|:---:|:---:|
  | 0 | 0 | 0 | **0** |
  | 0 | 1 | 1 | **1** |
  | 1 | 0 | 1 | **1** |
  | 1 | 1 | 1 | **0** |

### 4. Gerbang EX-NOR / Exclusive-NOR (IC 74266)
- **Logika:** **Genap/Sama = 1**. Kebalikan mutlak dari X-OR. Keluaran akan bernilai *High (1)* hanya apabila nilai semua inputnya **KEMBAR** (0 dan 0, atau 1 dan 1). Sering dipakai sebagai detektor kesamaan fasa/angka.
- **Persamaan Boolean:** $Y = \overline{A \oplus B}$ 
- **Tabel Kebenaran:**

  | Input A | Input B | Output Y (X-OR) | Output Y (X-NOR) |
  |:---:|:---:|:---:|:---:|
  | 0 | 0 | 0 | **1** |
  | 0 | 1 | 1 | **0** |
  | 1 | 0 | 1 | **0** |
  | 1 | 1 | 0 | **1** |

---

## Modul 3-4: Rangkaian Paralel Adder (Penjumlah) & Subtractor
Rangkaian digital yang bertugas melakukan operasi aritmatika penjumlahan biner dasar dan pengurangan menggunakan sistem komplemen.

### 1. Half Adder (HA)
Menjumlahkan **Dua Bit** data biner (A dan B). Memiliki 2 output: *Sum* (Hasil) dan *Carry-Out* (Sisa yang disimpan ke digit selanjutnya).
- **Sum (S):** Menggunakan gerbang **EX-OR** ($A \oplus B$). Dibuat memakai IC `7486`.
- **Carry (C):** Menggunakan gerbang **AND** ($A \cdot B$). Dibuat memakai IC `7408`.
> *Catatan:* Half Adder lemah karena tidak dapat menerima status *Carry-In* dari perhitungan kolom angka sebelumnya.

**Tabel Kebenaran Half Adder:**

| Input A | Input B | Carry Out (C) | Sum (S) |
|:---:|:---:|:---:|:---:|
| 0 | 0 | **0** | **0** |
| 0 | 1 | **0** | **1** |
| 1 | 0 | **0** | **1** |
| 1 | 1 | **1** | **0** | 

> **Ilustrasi Logika Gerbang HA (Kasus $A=1, B=1$):**
> - **Kabel S (Sum):** melewati gerbang EX-OR. $1 \oplus 1 = \mathbf{0}$. *(Lampu Sum mati)*
> - **Kabel C (Carry):** melewati gerbang AND. $1 \cdot 1 = \mathbf{1}$. *(Lampu Carry nyala)*. Ini merepresentasikan nilai desimal "2" dalam biner yaitu `10`.

### 2. Full Adder (FA)
Menjumlahkan **Tiga Bit** data biner sekaligus (Input A, Input B, dan *Carry-In* / Simpanan carry dari FA sebelumnya). 
- Dalam perakitan manual (*discrete*), FA disusun dari **dua buah Half Adder dan satu gerbang OR**.
- **IC Paralel Adder:** Secara praktikal di lab, diperkenalkan **IC 7483** yang merupakan sebuah chip *4-Bit Binary Full Adder* siap pakai. IC ini bisa langsung menjumlahkan 4 bit A ditambah 4 bit B.

**Tabel Kebenaran Full Adder:**

| Input A | Input B | Carry In (C_in) | Carry Out (C_out) | Sum (S) |
|:---:|:---:|:---:|:---:|:---:|
| 0 | 0 | 0 | **0** | **0** |
| 0 | 0 | 1 | **0** | **1** |
| 0 | 1 | 0 | **0** | **1** |
| 0 | 1 | 1 | **1** | **0** |
| 1 | 0 | 0 | **0** | **1** |
| 1 | 0 | 1 | **1** | **0** |
| 1 | 1 | 0 | **1** | **0** |
| 1 | 1 | 1 | **1** | **1** |

> **Ilustrasi Perolehan Tabel FA:**
> **1. Kasus 3 input menyala semua ($A=1, B=1, C_{\text{in}}=1$):**
> - Total nilai desimal $1+1+1 = \mathbf{3}$.
> - Biner angka 3 adalah `11`. Maka digit terakhir/Sum ($S$) = $\mathbf{1}$, dan digit depannya/Carry ($C_{\text{out}}$) = $\mathbf{1}$.
> 
> **2. Kasus hanya 2 input menyala ($A=1, B=0, C_{\text{in}}=1$):**
> - Total nilai desimal $1+0+1 = \mathbf{2}$.
> - Biner angka 2 adalah `10`. Maka digit belakang/Sum ($S$) = $\mathbf{0}$, sedangkan digit sisa dilimpahkan/Carry ($C_{\text{out}}$) = $\mathbf{1}$.

### 3. Operasi Pengurangan Biner dengan Komplemen
Chip logika (seperti Adder) aslinya tidak tahu cara mengurangi angka. Untuk melakukan operasi pengurangan (A - B), CPU mensiasati hal tersebut dengan menjumlahkan A dengan angka negatif B $\rightarrow A + (-B)$. Teknik mencari nilai negatif inilah yang disebut **Komplemen**.

- **Komplemen 1 (1's Complement):** Membalik (meng-_inverter_) keadaan seluruh bit. Angka `0` menjadi `1`, dan `1` menjadi `0`.
- **Komplemen 2 (2's Complement):** Hasil **Komplemen 1 ditambahkan 1** pada posisi bit urutan terbungsu (paling kanan / LSB). Semua PC modern memakai metode Komplemen-2 untuk memproses nilai minus hitungannya.

### Contoh Perhitungan Paralel Adder:
**A. Contoh Penjumlahan Menjulur lewat Full Adder (Contoh: $3 + 3 \rightarrow 011_2 + 011_2$)**
```text
  11      <-- Status limpahan Carry In (C_in) yang diumpan ke kolom sebelah kiri
  011 
  011
  --- +
  110     <-- Hasil Akhir Sum (Biner 110 = Desimal 6)
```

**B. Contoh Pengurangan menggunakan Komplemen-2 (Contoh: $5 - 2$)**
Kita ingin menghitung $5 - 2$. Di sini *A = 5*, *B = 2*.
1. Susun Nilai Asli Biner A (5) = `0101`
2. Susun Nilai Asli Biner B (2) = `0010`
3. Siapkan Nilai **Komplemen 2 dari B**:
   - Komplemen 1 dari B (balik $0010$) $\rightarrow$ menjadi `1101`
   - Komplemen 2 (Komplemen 1 ditambah `1`) $\rightarrow$ `1101` + `1` = `1110` *(Ini adalah wujud perwakilan -2)*
4. Eksekusi penjumlahan $A + (\text{Komplemen-2 B})$:
```text
   111      <-- Carry
   0101     (Ini bit utuh A yaitu 5)
   1110     (Ini bit negatif B / komplemen-2 dari 2)
   ---- +
  10011 
```
> **Aturan Emas Komplemen-2:** Karena format asal kita ada 4-bit, jika hasil output meluap hingga 5-bit `1 0011`, abaikan/buang Carry bit paling depan sebelah kiri (Overflow bit ke-5 dibuang).
Maka sisa output adalah: **`0011`**, yang bila disetorkan ulang ke format desimal bernilai mutlak **3** (Benar, sebab perhitungan asli $5 - 2 = 3$).

---

## Modul 5 & 6: Encoder dan Decoder
Dua rangkaian berlawanan fungsionalitas yang sangat penting untuk keperluan komunikasi *interface* antarmuka alat dan manusia (contoh: Keyboard dan Layar Seven Segment).

### Modul 5: Rangkaian Encoder
- **Definisi:** Rangkaian yang mengubah sinyal *input* desimal / input aktif yang banyak bentuknya, diringkas (dikodekan) ke dalam format *output* biner/BCD yang lebih sedikit letak kakinya (Meringkas $2^N$ jalur aktif menjadi $N$ jalur kode basis 2).
- **Contoh Analogi:** Tombol *keyboard* berangka 0-9 (10 kabel) di-encode menjadi format 4-bit biner yang masuk ke dalam prosesor.
- **Konfigurasi Lab (IC):** 
  - **IC 74147:** 10-line Decimal to 4-line BCD Priority Encoder.
  - **IC 74148:** 8-line Octal to 3-line Binary Priority Encoder.
  - *(Kamus: "Priority" maksudnya jika Anda menekan dua tombol bersamaan, nilai tertinggi yang akan diproses).*

**Tabel Data Percobaan Encoder (IC 74148 Active-Low)**
> *Catatan: IC 74148 adalah Priority Encoder bertipe Active-Low (Aktif saat diberi logika 0 / Ground).*

| Input EI | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | Output GS | Output EO | Output A2 | Output A1 | Output A0 |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | **1** | **0** | **1** | **1** | **1** |
| 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | **0** | **1** | **1** | **1** | **1** |
| 0 | X | 0 | 1 | 1 | 1 | 1 | 1 | 1 | **0** | **1** | **1** | **1** | **0** |
| 0 | X | X | 0 | 1 | 1 | 1 | 1 | 1 | **0** | **1** | **1** | **0** | **1** |
| 0 | X | X | X | 0 | 1 | 1 | 1 | 1 | **0** | **1** | **1** | **0** | **0** |
| 0 | X | X | X | X | 0 | 1 | 1 | 1 | **0** | **1** | **0** | **1** | **1** |
| 0 | X | X | X | X | X | 0 | 1 | 1 | **0** | **1** | **0** | **1** | **0** |
| 0 | X | X | X | X | X | X | 0 | 1 | **0** | **1** | **0** | **0** | **1** |
| 0 | X | X | X | X | X | X | X | 0 | **0** | **1** | **0** | **0** | **0** |
*(X = Don't Care / Terserah, karena ini PRIORITY encoder di mana nilai port urutan terbesar yang paling mendominasi menyala)*

### Modul 6: Rangkaian Decoder
- **Definisi:** Kebalikan dari Encoder. Ia menerima instruksi *input* biner ringkas ($N$ bit), lalu membongkarnya/membaca kode tersebut untuk mengaktifkan satu dari $2^N$ jalur *output* yang terpisah.
- **Contoh Analogi:** Mikrokontroler mengirim kode `0111` (7), Decoder kemudian menerjemahkan lalu menyalakan lampu-lampu LED panel di display 7-Segment untuk membentuk gambar angka 7.
- **Konfigurasi Lab (IC):** 
  - **IC 7447:** *BCD to 7-Segment Decoder/Driver* (Ini sangat wajib dihafal karena merupakan primadona lab saat membuat papan skor/jam digital di akhir semester). 

**Tabel Data Percobaan Decoder (IC 7447 to 7-Segment)**
*(Input berformat BCD (D, C, B, A) dikonversi untuk memicu lampu display meraga angka yang dimau)*

| Input D | Input C | Input B | Input A | Tampilan Angka BCD Pada Seven Segment |
|:---:|:---:|:---:|:---:|:---:|
| 0 | 0 | 0 | 0 | **0** |
| 0 | 0 | 0 | 1 | **1** |
| 0 | 0 | 1 | 0 | **2** |
| 0 | 0 | 1 | 1 | **3** |
| 0 | 1 | 0 | 0 | **4** |
| 0 | 1 | 0 | 1 | **5** |
| 0 | 1 | 1 | 0 | **6** |
| 0 | 1 | 1 | 1 | **7** |
| 1 | 0 | 0 | 0 | **8** |
| 1 | 0 | 0 | 1 | **9** |
| 1 | 0 | 1 | 0 | *(Simbol Error/Blank, krn BCD maksimal hanya batas 1001/9)* |
| 1 | 0 | 1 | 1 | *(Simbol Error/Blank)* |
| 1 | 1 | 0 | 0 | *(Simbol Error/Blank)* |
| 1 | 1 | 0 | 1 | *(Simbol Error/Blank)* |
| 1 | 1 | 1 | 0 | *(Simbol Error/Blank)* |
| 1 | 1 | 1 | 1 | *(Simbol Error/Blank)* |

---

## Modul 7 & 8: Multiplexer (MUX) & Demultiplexer (DEMUX)

### Modul 7: Multiplexer (Data Selector)
- **Definisi:** Rangkaian pemilih data. Menerima **banyak jalur input**, namun membiarkannya lolos ke **satu jalur output** tunggal secara bergantian.
- **Cara Kerja:** Ia dilengkapi dengan jalur pengendali (kaki *Selector/Select lines*). Misalnya ada 4 jalur *input*, maka butuh 2 pin *selector* ($2^2 = 4$) untuk menentukan kode input manakah yang mendapat giliran terhubung ke output utama. Layaknya saklar *switch* putar radio.
- **Konfigurasi Lab (IC):** **IC 74151** (8-line to 1-line Data Selector/Multiplexer, memiliki 8 input saluran data dan 3 jalur selektor pengendali).

### Modul 8: Demultiplexer (Data Distributor)
- **Definisi:** Kebalikan dari MUX. Menerima data dari **satu jalur input** secara sepihak, kemudian mendistribusikan data tersebut bercabang untuk diteruskan ke salah satu dari **banyak jalur output** yang dituju.
- **Cara Kerja:** Sangat mirip dengan *decoder*, dan kenyataannya IC De-Multiplexer secara fabrikasi seringkali berfungsi rangkap sebagai *Decoder*.
- **Konfigurasi Lab (IC):** **IC 74138** (Berfungsi sebagai *3-to-8 line Decoder* maupun sekaligus dikonfigurasi sebagai *Demultiplexer 1 ke 8 jalur* berkat adanya pin *Enable* di dalamnya).

---

## Modul 9, 10, & 11: Rangkaian Flip-Flop
Flip-Flop adalah komponen paling dasar dari sistem rangkaian digital **sekuensial** yang memiliki sifat "Mengingat" atau menyimpan satu bit data (Memori statis dasar). Berbeda dengan gerbang kombinasional (seperti AND/OR) yang *output*-nya langsung ganti saat *input* berubah, output Flip-Flop bergantung pada *input* detik ini AND keadaan memori (output) sebelumnya.

### Modul 9: S-R Flip-Flop (Set-Reset)
- **Definisi:** Memiliki dua input utama: **S (Set)** untuk membuat output (Q) menjadi 1, dan **R (Reset)** untuk membuat output (Q) menjadi 0.
- **Kondisi Terlarang:** Jika S dan R diberi nilai 1 secara bersamaan, output menjadi tidak valid atau tidak menentu (Invalid).
- **Konfigurasi Lab (IC):** Dibangun dari gabungan dua gerbang NAND (IC 7400) atau dua gerbang NOR (IC 7402) yang di-umpan balik (cross-coupled).

**Tabel Kebenaran S-R Flip-Flop**

| Clock (C) | Input S | Input R | Output $Q_{n+1}$ | Output $\overline{Q}_{n+1}$ | Kondisi / Keterangan |
|:---:|:---:|:---:|:---:|:---:|:---|
| $\uparrow$ | 0 | 0 | $Q_n$ | $\overline{Q}_n$ | **Tetap / No Change** (Mengingat keadaan sebelumnya) |
| $\uparrow$ | 0 | 1 | 0 | 1 | **Reset** |
| $\uparrow$ | 1 | 0 | 1 | 0 | **Set** |
| $\uparrow$ | 1 | 1 | - | - | **Invalid / Terlarang** |

### Modul 10: J-K Flip-Flop
- **Definisi:** Merupakan penyempurnaan dari S-R Flip-Flop untuk mengatasi "Kondisi Terlarang" (1 dan 1). Huruf J berperan seperti Set (S), dan K berperan seperti Reset (R).
- **Kondisi Toggle:** Jika J dan K sama-sama diberi logika 1, output akan berbalik keadaan dari status sebelumnya (Toggle / $Q_{n+1} = \overline{Q}_n$). Sifat inilah yang membuat J-K sangat berguna untuk rangkaian penghitung (Counter).
- **Konfigurasi Lab (IC):** **IC 7476** (Dual J-K Flip-Flop with Preset and Clear).

**Tabel Kebenaran J-K Flip-Flop**

| Clock (C) | Input J | Input K | Output $Q_{n+1}$ | Output $\overline{Q}_{n+1}$ | Kondisi / Keterangan |
|:---:|:---:|:---:|:---:|:---:|:---|
| $\uparrow$ | 0 | 0 | $Q_n$ | $\overline{Q}_n$ | **Tetap / No Change** |
| $\uparrow$ | 0 | 1 | 0 | 1 | **Reset** |
| $\uparrow$ | 1 | 0 | 1 | 0 | **Set** |
| $\uparrow$ | 1 | 1 | $\overline{Q}_n$ | $Q_n$ | **Toggle / Berubah Keadaan** (Solusi dari Invalid S-R) |

### Modul 11: D Flip-Flop (Data)
- **Definisi:** Flip-flop yang sangat sederhana, di mana output (Q) selalu mengikuti apa pun nilai yang diberikan pada input (D) tepat pada saat sinyal Clock (C) berdenyut.
- **Fungsi Utama:** Digunakan sebagai elemen penyimpan data sementara (Buffer/Register) untuk menahan nilai bit digital sinkron dengan *clock*.
- **Konfigurasi Lab (IC):** **IC 7474** (Dual D-Type Positive-Edge-Triggered Flip-flop).

**Tabel Kebenaran D Flip-Flop**

| Clock (C) | Input D | Output $Q_{n+1}$ | Output $\overline{Q}_{n+1}$ |
|:---:|:---:|:---:|:---:|
| $\uparrow$ | 0 | **0** | **1** |
| $\uparrow$ | 1 | **1** | **0** |

---

## Modul 12 & 13: Rangkaian Counter (Pencacah / Penghitung)
Aplikasi terbesar dari Flip-Flop sejagat raya adalah dijadikan fungsi pencacahan (*Counter*), seperti jam digital, indikator antrian mesin kasir, atau putaran tasbih digital.

### Modul 12: Asynchronous Counter (Pencacah Tak Serempak / Ripple Counter)
- **Cara Kerja Ciri Khas:** Flip-Flop pertama yang diberi asupan denyut *Clock* asli eksternal. Flip-flop rentengan selanjutnya TIDAK mendapatkan denyut jam itu secara langsung, melainkan mengambil/menumpang *clock* dari pin *output (Q)* flip-flop sebelumnya. Akibatnya aliran sinyal merambat lambat berurutan layaknya gelombang riak air (*ripple*).
- **Kelebihan & Kekurangan:** Konfigurasinya sangat mudah disusun (hanya menyambungkan seri J-K Flip-flop dalam kondisi *Toggle* `J=1, K=1`). Sisi negatifnya, terdapat *Propagation Delay* (Keterlambatan rambat) yang bisa menyebabkan *error* pada frekuensi/kecepatan tingkat tinggi.
- **Konfigurasi Lab (IC Utama):** **IC 7490** / 74LS90 (Ripple Decade Counter ber-modulus 10).
  - Chip ini berisi dua bagian mandiri: *Pembagi-2* dan *Pembagi-5*.
  - Untuk merakit *Decade Counter* (menggilir angka desimal 0 s.d 9), pin $Q_0$ harus dipasang nyambung ke pin input $CLK_1$ agar termodulasi menjadi 10-bit penuh. Tersedia input **MR** (*Master Reset* untuk memaksa kembali ke 0) dan **MS** (*Master Set*).
  - Umumnya di lab IC 7490 langsung disuntik masuk *(cascaded)* ke **IC 7447** (Decoder) agar bisa meraga wujud angkanya di layar 7-Segment.

### Modul 13: Synchronous Counter (Pencacah Serempak)
- **Cara Kerja Ciri Khas:** Seluruh jejeran gerbong memori Flip-Flop disuapi makan pulsa *Clock* utama secara **Bersamaan (Serentak)** tanpa ada diskriminasi kasta. Akibat sinkronisasi mutlak ini, semua memori bisa berpindah *state* sedetik bersama-sama tanpa cacat gantung (*delay rambat*).
- **Kelebihan & Kekurangan:** Sangat cepat dan presisi stabil pada skema perancangan mikroprosesor rumit. Kekurangannya adalah secara rangkaian di dalam chip jauh lebih kompleks (membutuhkan gerbang AND/OR berlapis untuk memandu logika lompatan pin J-K secara pintar).
- **Konfigurasi Lab (IC Utama):** **IC 74190** / 74LS190 (Synchronous UP/DOWN BCD Counter).
  - IC ini tidak cacat lambat, dan memiliki fitur penghitung dua arah (*UP / Naik* 0 ke 9 dan *DOWN / Turun* 9 ke 0) yang diatur melalui pin pengontrol **U/D**.
  - Punya pin masukan **$P_0 - P_3$ (Parallel Load)** yang sangat modern, sehingga *timer* bisa diprogram mulai jalan dari angka loncat yang tidak dari Nol (misal ditekan tombol langsung hitung mundur dari angka 5). 

---
### Susunan Hitungan BCD Counter (Modulus-10) untuk IC 7490 & 74190
Siklus perputaran pencacah berulang pada output digitalnya untuk mengendalikan lampu LED / Decoder desimal. Pada irama tepukan *clock* ke sepuluh, angka kembali mengulang ke `0000`.

| Denyut Clock ke- ($n$) | Output $Q_3$ | Output $Q_2$ | Output $Q_1$ | Output $Q_0$ | Nilai Displai Desimal |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 0 | 0 | 0 | 0 | 0 | **0** |
| $\uparrow$ 1 | 0 | 0 | 0 | 1 | **1** |
| $\uparrow$ 2 | 0 | 0 | 1 | 0 | **2** |
| $\uparrow$ 3 | 0 | 0 | 1 | 1 | **3** |
| $\uparrow$ 4 | 0 | 1 | 0 | 0 | **4** |
| $\uparrow$ 5 | 0 | 1 | 0 | 1 | **5** |
| $\uparrow$ 6 | 0 | 1 | 1 | 0 | **6** |
| $\uparrow$ 7 | 0 | 1 | 1 | 1 | **7** |
| $\uparrow$ 8 | 1 | 0 | 0 | 0 | **8** |
| $\uparrow$ 9 | 1 | 0 | 0 | 1 | **9** |
| $\uparrow$ 10 (Reset) | 0 | 0 | 0 | 0 | **0** |