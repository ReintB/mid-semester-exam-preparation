# Instrumentasi dan Pengukuran

## Daftar Isi
- [Bab 1: Dasar Instrumentasi](#bab-1-dasar-instrumentasi)
- [Bab 2: Pengetahuan Dasar Alat Ukur Listrik](#bab-2-pengetahuan-dasar-alat-ukur-listrik)
- [Bab 3: Dasar Sensor dan Transduser](#bab-3-dasar-sensor-dan-transduser)
- [Bab 4: Karakteristik Sensor](#bab-4-karakteristik-sensor)
- [Bab 5: Pengkondisi Sinyal](#bab-5-pengkondisi-sinyal)
- [Bab 6: Konversi Sinyal (ADC & DAC)](#bab-6-konversi-sinyal-adc--dac)

---

## Bab 1: Dasar Instrumentasi

### Sistem Akuisisi Data
Sistem Akuisisi Data secara umum terdiri dari:
1. **Sensor:** Alat pengindera/pengkonversi stimulus fisis.
2. **Pengkondisi Sinyal (Signal Conditioning):** Modifikasi sinyal mentah agar bisa diproses lebih lanjut.
3. **ADC (Analog to Digital Converter):** Pengubah sinyal fisika (analog) menjadi data biner (digital).
4. **Pemroses Sinyal:** Unit mikrokontroler/komputer yang melakukan komputasinya.
5. **Aktuator / Penampil (Display):** Penggerak/penyaji *output* ke lingkungan luar.

### Terminologi dan Definisi Penting
1. **Metrologi:** Ilmu pengetahuan yang berhubungan dan mempelajari tentang pengukuran.
2. **Instrumentasi:** Bidang ilmu (dan teknologi) meliputi perancangan, pembuatan, serta penggunaan instrumen untuk keperluan deteksi, pengukuran, serta pengolahan data.
3. **Pengukuran:** Rangkaian kegiatan eksperimen guna menentukan nilai kuantitatif sebuah besaran.
4. **Ketelitian (Accuracy):** Kemampuan alat ukur untuk memberikan indikasi / kedekatan dengan harga **nilai sebenarnya**.
5. **Ketepatan (Precision):** Kedekatan nilai-nilai pengukuran individual yang didistribusikan sekitar nilai rata-ratanya saat diulang.
6. **Sensitivitas (Sensitivity):** Perbandingan antara sinyal keluaran (respon) instrumen terhadap perubahan variabel masukan yang diukur.
7. **Repeatabilitas (Repeatability):** Kemampuan alat ukur untuk menunjukkan hasil yang sama dari proses pengukuran yang dilakukan berulang-ulang dan identik.
8. **Kesalahan (Error):** Penyimpangan variabel yang diukur dari nilai sebenarnya.
9. **Resolusi (Resolution):** Perubahan terkecil pada nilai yang diukur dari respon suatu instrumen.
10. **Kalibrasi (Calibration):** Serangkaian kegiatan memverifikasi/mencocokkan kebenaran indikasi ukur sebuah alat dengan membandingkannya ke standar ukur yang tertelusuri secara nasional/internasional.
11. **Koreksi (Correction):** Suatu harga aljabar yang ditambahkan pada hasil ukur untuk mengkompensasi penambahan kesalahan sistematik.
12. **Ketertelusuran (Traceability):** Terkaitnya hasil pengukuran pada standar nasional/internasional melalui peralatan ukur yang kinerjanya diketahui beserta sistem pembuktiannya.
13. **Kehandalan (Reliability):** Kesanggupan alat ukur untuk melaksanakan fungsi yang diisyaratkan untuk suatu periode yang ditetapkan.
14. **Ketidakpastian Pengukuran (Uncertainty):** Perkiraan atau taksiran rentang dari nilai pengukuran di mana nilai sebenarnya dari besaran obyek yang diukur terletak.
15. **Sensor:** Bagian/elemen dari alat ukur untuk mengubah suatu bentuk besaran fisik (sensing element) menjadi suatu **besaran listrik**.
16. **Transduser:** Bagian dari alat ukur yang mengubah suatu bentuk format energi menjadi **bentuk energi yang lain** sehingga mudah diolah oleh peralatan berikutnya.
17. **Rentang ukur (Range):** Besar daerah ukur di antara batas ukur bawah dan batas ukur atas.
18. **Jangkauan (Span):** Beda modulus antara dua batas rentang nominal dari alat ukur (Contoh: Bekerja pada rentang -10V sampai 10V, maka Span = 20V).

---

## Bab 2: Pengetahuan Dasar Alat Ukur Listrik

### 1. Besaran Listrik Dasar
- **Arus Listrik (I):** Aliran muatan listrik dalam suatu penghantar, dihitung dengan satuan Ampere (A). Arus mengalir dikarenakan adanya sumber tegangan (voltage) yang terhubung dalam suatu sistem tertutup, yang juga memiliki hambatan (resistansi).
- **Tegangan (E/V):** Besarnya gaya pendorong aliran arus (Electromotive Force), bersatuan Volt (V). Tegangan muncul berkat perbedaan potensial antara dua kutub (kutub positif untuk potensial tinggi, dan kutub negatif untuk potensial rendah).

### 2. Galvanometer
- Merupakan alat ukur dasar atau komponen pengerak utama di dalam berbagai instrumen ukur listrik tipe jarum penunjuk (analog).
- Galvanometer bekerja berdasarkan prinsip interaksi medan magnet. Arus listrik yang dilewatkan pada sebuah kumparan (coil) di dalam medan magnet permanen akan menghasilkan gaya Lorentz, yang berujung membangkitkan momen torsi (putaran) penggerak jarum ke satu arah tertentu atau diistilahkan simpangan. 

### 3. Penggunaan Sebagai Alat Ukur Varian Lain
Dari basis pergerakan *movement* Galvanometer ini, bisa direkayasa lebih luas dengan penambahan susunan tahanan (resistor) agar kemampuannya lebih spesifik:
- **Amperemeter:** Galvanometer yang dipararelkan dengan sebuah tahanan *Shunt* bernilai ukur kecil (sangat rendah). Fungsinya agar alat ini bisa mengukur laju kuat arus besar tanpa merusak kumparan dalamnya. Di rangkaian, Amperemeter harus **dipasang secara Seri** dengan beban yang akan diuji.
- **Voltmeter:** Galvanometer diserikan bersama dengan tahanan *Multiplier* yang bernilai sangat besar (tinggi). Ini memungkinkannya mengukur besarnya perbedaan tegangan rangkaian yang nilainya lebih tinggi. Di rangkaian, Voltmeter selalu **dipasang secara Paralel**.
- **Ohmmeter:** Terdapat tambahan sumber power/baterai lokal di dalam alat untuk menginjeksi listrik ke komponen yang diuji demi mengetahui seberapa besar nilai resistornya.

### 4. Multimeter
Sering disebut pula AVO-meter (Ampere-Volt-Ohm), yaitu alat uji portabel serbaguna yang menyatukan fungsi Voltmeter, Amperemeter, beserta Ohmmeter dalam 1 wadah yang sama. Penggunanya hanya cukup mengubah posisi *knob* ke fungsi mana yang hendak diperlukan saat *troubleshooting* atau mengukur rangkaian.

---

## Bab 3: Dasar Sensor dan Transduser

### Definisi Sensor & Transduser
- **Sensor:** Perangkat yang menerima stimulus dan merespon dengan mengeluarkan sinyal elektronik (Tegangan, Arus, Tahanan) dengan merubah besaran fisis menjadi besaran listrik.
- **Transduser:** Perangkat yang merubah besaran fisis menjadi besaran fisis yang lain (seperti energi). Sebuah transduser dapat juga dihubungkan dengan *aktuator* (pengubah listrik kembali menjadi gerakan fisis, misal: motor listrik).

### Tipe Konversi & Sistem Sensor
Modifikasi pengubahan besaran ini dapat terjadi via:
1. **Sensor Langsung (Direct):** Mengubah stimulus langsung menjadi sinyal listrik lewat 1 efek fisika.
2. **Sensor Kompleks:** Melalui lebih dari 1 tahapan konversi transduser sebelum jadi sinyal akhir.

### Klasifikasi Sensor
Terdapat berbagai cara mengklasifikasikan sifat sensor, antara lain:

**1. Berdasar Kedudukan Acuan Pengukuran (Referensi):**
- **Sensor Absolut:** Sensor mendeteksi stimulus mandiri pada skala fisis murni independen. *(Contoh: Termistor yg resistansinya berhubungan dgn skala temperatur absolut Kelvin/Celcius).*
- **Sensor Relatif:** Sensor yang mengukur berdasar kasus khusus / referensi banding gradien tertentu. *(Contoh: Termokopel menghasilkan tegangan sebagai fungsi dari gradien temperatur persimpangannya).*

**2. Berdasar Ketergantungan Suplai Energi:**
- **Sensor Aktif:** Membutuhkan injeksi sumber daya luar (sinyal eksitasi) agar aktif dan responsif. *(Contoh: Termistor).*
- **Sensor Pasif:** Secara alami memproduksi energi sinyal listrik dari materialnya tanpa dicatu daya eksternal. *(Contoh: Termokopel, Fotodioda, Piezoelektrik).*

---

## Bab 4: Karakteristik Sensor

Pemahaman mengenai spesifikasi dan cara pembacaan *datasheet* sensor memuat berbagai parameter operasional, di antaranya:

### Karakteristik Statis
1. **Fungsi Transfer:** Hubungan matematis ideal antara sinyal input fisis (stimulus) dengan output listrik. Beberapa rumusan dasarnya:
   - Hubungan Linier: $S = a + bs$
   - Fungsi Logaritmik: $S = a + b \ln s$
   - Fungsi Eksponensial: $S = a e^{bs}$
   - Fungsi Pangkat: $S = a_0 + a_1 s^b$
   - Radiasi Termal (Inframerah): $V = G \left( T_b^4 - T_s^4 \right)$
   *(Keterangan: S = Sinyal keluaran, s = Sinyal masukan, b = Sensitivitas, $G$ = Konstanta, $T_b$ & $T_s$ = Temperatur Absolut)*
2. **Span (Range) & FSO:** *Span/Range* adalah besaran jangkauan dinamis input minimum hingga maksimum yang mampu diproses oleh sensor (juga disebut *Input Full Scale/FS*). FSO (*Full Scale Output*) adalah selisih *output* antara pembacaan input maksimum dengan minimum.
3. **Inakurasi / Error:** Taraf/persentase deviasi tertinggi keluaran praktis sensor terhadap nilai hitung standarnya. 
   $$\text{Inakurasi (\%)} = \left(\frac{\text{Penyimpangan max}}{\text{Span Input}}\right) \times 100\%$$
4. **Histeresis:** Ketidakcocokan pembacaan pada poin yang sama saat input sedang gerak naik (mendekat) dibandingkan saat grafiknya gerak turun kembali (menjauh).
5. **Ketidaklinearan (Non-Linearity):** Simpangan kurva keluaran riil sensor terhadap grafik linier acuan idealnya.
6. **Saturasi (Saturation):** Batas rentang ukur tertinggi operasional di mana sensor sudah tidak merespons normal (nilainya sudah konstan/mendatar).
7. **Pita Mati (Dead Band):** Daerah/rentang inisial di mana perubahan masukan stimulus belum sanggup membangkitkan respon sinyal *output* sama sekali.
8. **Resolusi:** Perubahan input paling kecil yang sudah dapat dideteksi perbedaannya secara presisi di layar.
9. **Kesalahan Berulang:** Penyimpangan/kegagalan sensor menghasilkan angka *output* yang persis *identik* pada saat diuji pengukuran pada nilai kondisi fisis yang sama berulang-ulang (bisa karena penumpukan *noise* atau elastisitas material memudar).

### Faktor Dinamis & Lingkungannya
- **Eksitasi:** Besar sinyal listrik yang diperlukan men- *trigger* sensor aktif.
- **Karakteristik Tundaan & Respon Waktu (Dinamik):** Bergantungnya kurva pembacaan terhadap limitasi *Cut-off Frequency* atau respon orde nol, 1, dan 2 dari sensor dalam menyesuaikan dengan perubahan cepat.
- **Batasan Lingkungan & Ketahanan:** Stabilitas *Short Term* (menghadapi noise frekuensi rendah sementara) dan *Long Term* (keausan bahan dari umur/lingkungan suhu ekstrim sekitar).

---

## Bab 5: Pengkondisi Sinyal

Berfungsi untuk memproses dan menyesuaikan sinyal keluaran dari sensor sebelum dibaca/diproses lebih lanjut (terutama oleh instrumen komputasi).

### 1. Rangkaian Pembagi Tegangan (Voltage Divider)
Merupakan sirkuit dasar yang disusun oleh dua atau lebih komponen *resistor* yang dirangkai secara seri. Fungsinya untuk mengubah tegangan masukan (*Voltage Input*) yang besar menjadi tegangan keluaran ukur yang lebih kecil secara proporsional sesuai nilai hambatannya. Rumus dasarnya adalah:
$$V_{out} = V_{in} \times \left( \frac{R_1}{R_1 + R_2} \right)$$
*(Di mana $V_{out}$ adalah tegangan yang diukur pada hambatan $R_1$)*

### 2. Konverter Arus Ke Tegangan (I/V Converter)
Komponen fungsional yang mengubah besaran arus elektrik (I) menjadi besaran tegangan (V). Contoh aplikasinya adalah pada *Photodetector Amplifier* yang digunakan untuk menampung besaran arus *output* kecil dari fotodioda menjadi tegangan (Voltage). Persamaan keluaran $V_o$ dari transkonduktansi ini adalah:
$$V_o = -i \cdot R_F$$
*(Di mana $i$ = Arus sumber, $R_F$ = Nilai Tahanan Feedback)*

### 3. Operational Amplifier (Op-Amp)
Suatu komponen sirkuit penguat diferensial berefisiensi tinggi untuk membesarkan (amplifikasi) sinyal-sinyal amplitudo lemah dari pendeteksi fisik. Op-Amp memakai kaki polaritas positif dan negatif tegangan rel $V_{cc}$ ($V_{sat}$), yang gelombang *output*-nya dibatasi dan tidak melampaui catu daya puncaknya. Beberapa rumusan konfigurasi Op-Amp adalah:
- **Penguat Membalik (Inverting):** Menguatkan sinyal masukan namun hasil fase keluarannya berbalik arah ujung 180° terhadap masukannya (mempunyai perbandingan gain negatif).
  $$V_{out} = -\left( \frac{R_F}{R_{in}} \right) V_{in}$$
- **Penguat Tak Membalik (Non-Inverting):** Menguatkan amplitudo sinyal tanpa mengganti/membalik polaritas dan perbedaan fasenya.
  $$V_{out} = \left( 1 + \frac{R_F}{R_{in}} \right) V_{in}$$

### 4. Filter Frekuensi (Rangkaian RC & Low/High Pass Filter)
Variasi Op-Amp sering juga dilengkapi oleh sirkuit pasif seperti resistor (R) dan kapasitor (C) untuk menyaring / melemahkan noise (sebagai *Filter Aktif*). Rumus umum titik *Cut-off Frequency* ($f_c$) filter orde pertama:
$$f_c = \frac{1}{2 \pi R C}$$

---

## Bab 6: Konversi Sinyal (ADC & DAC)

### Perbedaan Format Sinyal Elektronik
- **Sinyal Analog:** Sinyal listrik dengan rentang amplitudo terhadap alur waktu yang bergerak wujudnya secara logis dan *kontinu*.
- **Sinyal Digital:** Wujud representasi serpihan sinyal diskrit / patah-patah terhadap rentang waktu tertentu. Dimodulasi menggunakan *PCM (Pulse Code Modulation)* menjadi nilai Biner `0` dan `1`.

### Konverter Perantara
1. **ADC (Analog to Digital Converter):** Proses mentransformasi tegangan *Analog* dari sensor ukur menjadi deretan langkah bilangan desimal & *Digital* ke prosessor. Persamaan konversinya:
   $$V_{out(\text{Desimal})} = \left( \frac{V_{in}}{V_{ref}} \right) \times ADC_{\text{max}}$$
   *(Catatan: Langkah terakhir ini wujud nilai desimal yang nantinya dikoversi biner)*
2. **DAC (Digital to Analog Converter):** Memutarbalikkan manipulasi *Digital* Biner dari mikrokontroler agar kembali memompa level diskrit menjadi *staircase Analog*. Rumusnya mirip namun sebagai pembangkit Output tegangan fisika:
   $$V_{out} = \left( \frac{Input_{\text{DAC}}}{DAC_{\text{max}}} \right) \times V_{ref}$$
   *(Keterangan: $V_{ref}$ adalah tegangan referensi maksimum, misal 5V)*

### Tingkat Resolusi & Pengolahan ADC Data
Kualitas transisi konversi bergantung rentang nilai hitung resolusinya. Limitasi maksimal dari pencacahan ($ADC_{\text{max}}$) diatur spesifikasi panjang "Bit", seperti:
- **Konverter 8-Bit:** Menyediakan $2^8 = 256$ skala pencacahan (dari indeks `0` hingga target maksimum `255`).
  $$ADC_{\text{max}} = 255$$
  $$\text{Resolusi 8-Bit} = \frac{V_{ref}}{ADC_{\text{max}}}$$
- **Konverter 10-Bit:** Menyediakan $2^{10} = 1024$ skala cacahan (indeks `0` hingga target maksimum `1023`).
  $$ADC_{\text{max}} = 1023$$
  $$\text{Resolusi 10-Bit} = \frac{V_{ref}}{ADC_{\text{max}}}$$

**Resolusi:** Merupakan lonjakan/celah varian tegangan paling renik yang mendeteksi perubahan transisi nilai 1 bit.
Sebagai ilustrasi untuk $V_{ref} = 5\text{V}$:
- **ADC 8-Bit:** Loncatan pertambahan per langkah (1 bit) adalah $= \frac{5}{255} \approx 0,019 \text{ Volt}$.
- **ADC 10-Bit:** Pertambahan pencacah setiap skala nilai (1 bit) adalah $= \frac{5}{1023} \approx 0,005 \text{ Volt}$. Resolusi pada sistem ini terbukti lebih rapat (tinggi) & presisi, dengan trade-off memakan beban *byte memory* sirkuit yang jelas lebih raksasa.

---

---
[<< 07 - Praktikum Elektronika Digital](../07%20-%20Praktikum%20Elektronika%20Digital/README.md) | [HOME](../README.md) | [09 - Mesin - Mesin Listrik >>](../09%20-%20Mesin%20-%20Mesin%20Listrik/README.md)