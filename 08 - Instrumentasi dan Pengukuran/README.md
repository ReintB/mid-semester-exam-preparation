# Instrumentasi dan Pengukuran

## Daftar Isi
- [Bab 1: Dasar Instrumentasi](#bab-1-dasar-instrumentasi)
- [Bab 2: [Modul Belum Ada]](#bab-2-modul-belum-ada)
- [Bab 3: Dasar Sensor dan Transduser](#bab-3-dasar-sensor-dan-transduser)

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

## Bab 2: [Modul Belum Ada]

---

## Bab 3: Dasar Sensor dan Transduser

### Perbedaan Utama:
- **Sensor:** Merubah stimulus fenomena energi fisis di alam secara khusus menjadi output **besaran sinyal elektronik** yang terukur (seperti: Tegangan/Voltage, Arus/Ampere, Resistansi/Tahanan).
- **Transduser:** Mengubah variabel fisik spesifik menjadi variabel fisik yang lain (biasanya butuh tahapan lanjut untuk dimonitor elektronik).
- **Aktuator:** Berperan layaknya "aktor/pelaksana". Kebalikan sensor; mengubah besaran pemicu listrik kembali menjadi bentuk efek pergerakan fisis (cth: Motor DC membungkus listrik jadi kinetik gerak mekanikal).

### Persyaratan Umum Sensor dan Transduser
Agar sebuah sensor / transduser dapat bekerja dengan baik dalam suatu sistem pengukuran, diperlukan kualitas dengan batasan berikut:
1. **Linearitas:** Tanggapan keluaran idealnya linier (proporsional) terhadap masukan. Semakin linier, konversi data lebih mudah diolah.
2. **Sensitivitas:** Rasio unit perubahan keluaran banding unit perubahan masukan (cth: naik 1 derajat menghasilkan 1 Volt tegangan keluaran).
3. **Respon Waktu:** Kemampuan sensor bereaksi terhadap perubahan input parameter seiring berjalannya waktu (sebaiknya cepat merespon).

### Pertimbangan Tambahan Memilih Sensor
1. Ukuran fisik (harus pas di area pemasangan).
2. Memiliki tingkat akurasi tinggi dan beroperasi pada jangkauan / rentang yang sesuai.
3. **Non-Intrusif / Tidak mempengaruhi obyek ukur** (Contoh: Sensor panas besar yang diletakkan pada air sedikit akan malah menghangatkan air, bukan mengukur aslinya).
4. Sanggup bertahan / tangguh di lingkungan pemakaiannya (suhu ekstrim, dsb).
5. Biaya yang efektif.

### Klasifikasi Sensor
Terdapat berbagai cara mengklasifikasikan sifat sensor, antara lain:

**1. Berdasar Kedudukan Acuan Pengukuran (Referensi):**
- **Sensor Absolut:** Sensor merekam dan mendeteksi stimulus dengan mereferensikan pengukurannya langsung ke titik pangkal nol absolut bebas independen. *(Contoh: Termistor yang mengukur langsung temperatur absolut Kelvin).*
- **Sensor Relatif:** Sensor yang mengukur tingkat deviasi/perbedaan berdasarkan gradient lokal/kasus tertentu. *(Contoh: Termokopel membaca temperatur layaknya perbandingan tingkat pemanasan di dua buah persimpangan kawat material logam).*

**2. Berdasar Ketergantungan Suplai Energi:**
- **Sensor Aktif (Parametrik):** Membutuhkan injeksi sumber daya luar (sinyal eksitasi) agar sensor tersebut responsif dan bisa berfungsi mengirim sinyal. *(Contoh: Termistor).*
- **Sensor Pasif (Self-Generating):** Secara alami langsung memproduksi energi sinyal listrik dari material sensornya itu sendiri murni akibat stimulus fisis yg diserap dan tidak memerlukan energi catu daya eksternal. *(Contoh: Termokopel, Piezoelektrik yang menghasilkan voltase saat disentuh, atau dioda fotovoltaik).*

**3. Berdasar Jenis Sinyal Keluaran:**
- **Sensor Analog:** Mengeluarkan fluktuasi sinyal kontinu (cth: LVDT, Thermokopel, RTD, Strain gage, Load cell).
- **Sensor Digital:** Mengeluarkan nilai diskrit / biner secara langsung (cth: Rotary encoder).
- **Sensor ON/OFF:** Mengeluarkan sinyal batas *discrete trigger* antara nyala/mati (cth: Proximity sensor (kapasitif/induktif), limit switch).

**4. Berdasar Tahapan Proses Pengubahan:**
- **Sensor Langsung (Direct):** Secara instan memodifikasi efek fisika jadi listrik.
- **Sensor Kompleks:** Terdiri dari rantaian satu/lebih transduser dalam mendapatkan hasil listriknya.

---

---
[<< 07 - Praktikum Elektronika Digital](../07%20-%20Praktikum%20Elektronika%20Digital/README.md) | [HOME](../README.md) | [09 - Mesin - Mesin Listrik >>](../09%20-%20Mesin%20-%20Mesin%20Listrik/README.md)
