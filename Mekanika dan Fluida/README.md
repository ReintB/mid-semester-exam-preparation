# Mekanika dan Fluida

## Daftar Isi
- [1. Informasi Umum dan Istilah Penting](#1-informasi-umum-dan-istilah-penting)
- [2. Rumus-Rumus Inti dan Satuan](#2-rumus-rumus-inti-dan-satuan)
- [3. Contoh Soal dan Pembahasan Singkat](#3-contoh-soal-dan-pembahasan-singkat)

---

## 1. Informasi Umum dan Istilah Penting

- **Fluida Statis:** Cabang mekanika fluida yang mempelajari fluida yang diam (tidak mengalir secara makroskopis). Kajian utamanya mencakup **tekanan hidrostatis**, **Pascal**, dan **gaya apung / Archimedes**.
- **Fluida Dinamis:** Mempelajari fluida yang bergerak atau mengalir (pengukuran aliran). Analisis utamanya didasarkan pada kekekalan massa aliran (kontinuitas) dan kekekalan energi mekanik (Bernoulli).
- **Massa Jenis / Densitas ($\rho$):** Perbandingan rasio massa benda per satuan volume. (Satuan SI: $$ \text{kg/m}^3 $$).
- **Specific Gravity (Berat Jenis):** Perbandingan antara massa jenis suatu zat dengan massa jenis air murni referensi ($\rho_{\text{air}} = 1000 \, \text{kg/m}^3$ pada suhu $4^\circ\text{C}$). Sifatnya tak bersatuan.
- **Tekanan ($P$):** Gaya normal (tegak lurus) yang bekerja pada suatu permukaan per satuan luas. (Satuan SI: Pascal atau $\text{Pa}$. Dimana $1 \, \text{Pa} = 1 \, \text{N/m}^2$, dan nilai $1 \, \text{atm} \approx 1,013 \times 10^5 \, \text{Pa}$).
- **Debit Aliran ($Q$):** Volume zat fluida yang mengalir melintasi suatu penampang pipa/saluran dalam satuan waktu. (Satuan SI: $\text{m}^3/\text{s}$).
- **Viskositas ($\eta$):** Ukuran "kekentalan" fluida, yang merepresentasikan resistansi atau gesekan internal lapisan fluida saat bergerak.

---

## 2. Rumus-Rumus Inti dan Satuan

### A. Konsep Fluida Statis (Giancoli Ch 10)
1. **Massa Jenis (Density):**  
   $$ \rho = \frac{m}{V} $$
   - $\rho$ = Massa jenis / Densitas ($\text{kg/m}^3$)

2. **Massa dan Berat Suatu Benda:**  
   Berdasarkan volume suatu benda solid maupun cairan, massa dan beratnya adalah:
   - **Massa ($m$):** $m = \rho \cdot V$ 
   - **Berat ($W$):** $W = m \cdot g = \rho \cdot V \cdot g$ 

3. **Tekanan (Pressure) Secara Umum:**  
   Tekanan adalah gaya per satuan luas.
   $$ P = \frac{F}{A} $$ 

4. **Tekanan Hidrostatis (Tekanan Dalam Cairan Diam) dan Tekanan Gauge:**  
   - **Tekanan Mutlak/Total:** $P = P_{atm} + \rho g h$
   - **Tekanan Gauge (Tekanan Terukur):** Selisih tekanan total dengan tekanan batasan atmosfer (tekanan ukur oleh alat).
     $$ P_{gauge} = P - P_{atm} = \rho g h $$

5. **Prinsip Pascal (Pascal's Principle):**  
   "Tekanan ekstra yang diberikan pada fluida tertutup akan diteruskan secara seragam sebanding ke seluruh arah permukaan."  
   $$ P_1 = P_2 \implies \frac{F_1}{A_1} = \frac{F_2}{A_2} $$

6. **Hukum Archimedes (Gaya Apung / Buoyancy):**  
   $$ F_A = \rho_{\text{fluida}} \cdot g \cdot V_{\text{tercelup}} $$

### B. Konsep Fluida Dinamis & Fluida Riil (Viskositas)

1. **Mass Flow Rate (Laju Aliran Massa):**  
   Massa fluida yang mengalir melewati suatu titik dalam satu rentang waktu tertentu.
   $$ \frac{\Delta m}{\Delta t} = \rho A v $$

2. **Persamaan Kontinuitas (Volume Flow Rate):**  
   Untuk fluida inkompresibel (seperti air), laju massa konstan sehingga debit ($Q$) kekal dan berlaku:
   $$ Q = A_1 \cdot v_1 = A_2 \cdot v_2 $$

3. **Persamaan Bernoulli (Kekekalan Energi Mekanik):**  
   Cerminan perpaduan atas Kerja Tekanan, Energi Kinetik aliran, dan Energi Potensial letak.
   $$ P_1 + \frac{1}{2}\rho v_1^2 + \rho g y_1 = P_2 + \frac{1}{2}\rho v_2^2 + \rho g y_2 $$

4. **Teorema Torricelli (Tangki Bocor):**  
   Kecepatan fungsional debit bebas fluida sejauh $h$ berbanding lurus dari posisi lubukannya.
   $$ v = \sqrt{2 g h} $$

5. **Viskositas (Kekentalan, $\eta$):**  
   Resistansi aliran dinamik. Besarnya gaya $F$ yang diperlukan untuk menggeser plat batas seluas $A$ dengan kelajuan $v$ atas jarak $L$ rongga tabung.
   $$ F = \eta A \frac{v}{L} $$
   - $\eta$ = Koefisien Viskositas fluida ($\text{Pa}\cdot\text{s}$ atau $\text{N}\cdot\text{s/m}^2$)

6. **Persamaan Poiseuille (Poiseuille's Equation):**  
   Model matematika nyata laju penampang debit tabung tertutup (pipa viskos).
   $$ Q = \frac{\pi R^4 (P_1 - P_2)}{8 \eta L} $$

---

### C. Analisis Rejim Aliran dan Metode Pengukuran (Obstruction Methods)

1. **Jenis (Rejim) Aliran Berdasarkan Bilangan Reynolds (Re):**
   - **Aliran Laminer ($Re \le 2000$):** Partikel zat cair bergerak teratur mengikuti lintasan saling sejajar. (Kekentalan besar atau kecepatan kecil).
   - **Aliran Transisi ($2000 < Re < 4000$):** Fase peralihan dari lurus menjadi tidak beraturan.
   - **Aliran Turbulen ($Re \ge 4000$):** Gerak partikel acak tidak teratur (Kecepatan besar dan kekentalan cair kecil).

2. **Pola Aliran (Flow Regime) Campuran (Cair & Gas):**
   - **Bubbly Flow:** Gelembung gas di dalam fluida cair.
   - **Plug Flow:** Gas cukup besar membentuk gumpalan "plug" masuk dalam aliran fluida.
   - **Stratified Flow:** Gas mengalir di lapisan atas fluida cair dengan kecepatan lebih tinggi.
   - **Slug Flow:** Kecepatan tinggi yang memerangkap gas menjadi kantung dan menyebabkan getaran besar pad pipa (*slugging*).

3. **Metode Rintangan (Obstruction Methods):**
   Metode mengukur laju aliran dengan sengaja memberikan penyempitan hambatan pada pipa untuk memanfaatkan perbedaan *(drop) pressure* atau efek Bernoulli. Beberapa perlakuan standar:
   - **Plat Orifice (Orifice):** Menggunakan plat melingkar berlubang. Sederhana namun beda tekanan bisa hilang secara permanen cukup besar.
   - **Venturi Tube (Efek Venturi):** Penyempitan bertahap/halus, akurasinya tinggi dan *pressure loss* minim.
   - **Pitot Tube:** Tabung berujung ke arah mata aliran untuk membaca *stagnation pressure* (tekanan dinamik+statis).

   **Rumus Umum Aliran Obstruction:**
   $$ Q = C_d \frac{\pi}{4} D_2^2 \sqrt{\frac{2\Delta P}{\rho (1 - d^4)}} $$
   - $Q$ = Laju aliran volume (Debit sesungguhnya)
   - $C_d$ = *Discharge Coefficient* (koefisien laju buang empiris). Pada standar *Orifice* banyak diambil angka $C_d \approx 0.60$, tetapi dapat bervariasi tergantung bilangan Reynolds maupun rasio d.
   - $\Delta P$ = Perbedaan/Drop tekanan ($P_1 - P_2$)
   - $D_1, D_2$ = Diameter penampang besar pipar dan penampang *obstruction* (hambatan)
   - $d$ = Besaran rasio penyempitan ($d = \frac{D_2}{D_1}$)

---

### D. Tabel Referensi Bahan Fluida

#### 1. Tabel Konstanta Densitas ($\rho$) Berbagai Material
Nilai ini didasarkan pada temperatur normal ($\approx 20^\circ\text{C}$), referensi standar buku Giancoli.

| Material | Massa Jenis ($\rho$) dalam kg/m³ | Massa Jenis ($\rho$) dalam g/cm³ |
| :--- | :---: | :---: |
| **Aluminium** | $2.70 \times 10^3$ | $2.70$ |
| **Iron** (Besi) | $7.8 \times 10^3$ | $7.8$ |
| **Copper** (Tembaga) | $8.9 \times 10^3$ | $8.9$ |
| **Lead** (Timbal) | $11.3 \times 10^3$ | $11.3$ |
| **Air Murni** (Water pada $4^\circ\text{C}$) | $1.00 \times 10^3$ | $1.00$ |
| **Udara** (Air pada 1 atm) | $1.29$ | $0.00129$ |

#### 2. Tabel Koefisien Viskositas ($\eta$)
Nilai gesekan viskositas berubah bergantung kepada temperatur cairan sekitarnya (1 $\text{Pa}\cdot\text{s} = 10 \text{ Poise}$).

| Tipe Fluida (Cairan / Gas) | Suhu ($^\circ\text{C}$) | Koefisien Viskositas ($\eta$) dalam Pa$\cdot$s |
| :--- | :---: | :---: |
| **Air Cair** (Water) | $0$ | $1.8 \times 10^{-3}$ |
| **Air Cair** (Water) | $20$ | $1.0 \times 10^{-3}$ |
| **Air Cair** (Water) | $100$ | $0.3 \times 10^{-3}$ |
| **Darah Utuh** (Whole Blood) | $37$ | $\sim 4 \times 10^{-3}$ |
| **Udara** (Air gas) | $20$ | $0.018 \times 10^{-3}$ |
| **Oli Mesin** (Motor Oil SAE 10) | $30$ | $\sim 200 \times 10^{-3}$ |
| **Gliserin** (Glycerin) | $20$ | $1.5$ |

---

## 3. Contoh Soal dan Pembahasan Singkat

### Soal 1: Dongkrak Lift Mobil Canggih (Hukum Pascal)
Sebuah dongkrak hidraulik mempunyai piston kecil seluas penampang $10 \, \text{cm}^2$ guna mengangkat mobil di piston besar berpenampang $400 \, \text{cm}^2$. Supaya mampu mengimbangi angkatan beban massa bermobil seberat $16.000 \, \text{N}$, gaya $(F_1)$ minimal yang harus memompa dorongan piston kecil adalah?

**Pembahasan:**
Diketahui $A_1 = 10 \, \text{cm}^2$, $A_2 = 400 \, \text{cm}^2$, tegangan atas lift $F_2 = 16000 \, \text{N}$. (Satuan luasan tidak perlu dikonversi ke $m^2$ asal rasio perbandingannya tetap sama). Berdasarkan hukum distribusi rata Pascal:
$$ \frac{F_1}{A_1} = \frac{F_2}{A_2} \implies F_1 = F_2 \times \frac{A_1}{A_2} $$
$$ F_1 = 16000 \times \frac{10}{400} = 16000 \times \frac{1}{40} = 400 \, \text{N} $$

### Soal 2: Persamaan Kontinuitas Aliran Reduksi Pipa 
Air sungai dialirkan pada sebuah Pipa horizontal yang bagian awalnya berdiameter  $D_1 = 10 \, \text{cm}$ kemudian pipanya direduksi mengerucut menjadi berdiameter $D_2 = 5 \, \text{cm}$. Bila pada area pipa yang lebih lebar, alat pencatat flowmeter terbaca mendeteksi rata aliran laju sebesar $4 \, \text{m/s}$, hitunglah rata laju jatuhnya air $v_2$  yang diproyeksikan pada bagian reduksi sempit pipa?

**Pembahasan:**
Luas permukaan penampang berbentuk pipa silinder bundar bernilai ekuivalen pada $A = \frac{\pi}{4} D^2$. Berarti $A$ nilainya sebanding kuadrat diameter ($A \propto D^2$).
$$ A_1 \cdot v_1 = A_2 \cdot v_2 $$
$$ (D_1)^2 \times v_1 = (D_2)^2 \times v_2 $$
$$ (10)^2 \times 4 = (5)^2 \times v_2 $$
$$ 100 \times 4 = 25 \times v_2 $$
$$ v_2 = \frac{400}{25} = 16 \, \text{m/s} $$
*(Catatan Analisis: Luasan diameter pipa mengecil setengan kali, berdampak arusnya berjalan 4x berlipat lebih sangat cepat mengompensasi).*

### Soal 3: Teorema Torricelli (Debit semburan kecepatan curah)
Terdapat wadah tangki menampung debit cadangan suplai air, celah keretakan selang tangki tersebut tembus melubangi tabung 5 meter lurus di bawah batas permukaan air genangan puncak. Laju kecepatan dorong aliran keluarnya resapan air adalah? ($g = 9.8 \, \text{m/s}^2$).

**Pembahasan:**
Memakai hukum pembuktian instan Torricelli:
$$ v = \sqrt{2 \cdot g \cdot h} $$
$$ v = \sqrt{2 \times 9.8 \times 5} = \sqrt{98} \approx 9.899 \, \text{m/s} $$
