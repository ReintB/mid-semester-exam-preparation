# Mesin-Mesin Listrik

## Daftar Isi
- [1. Konsep Dasar Konversi Elektromagnetik](#1-konsep-dasar-konversi-elektromagnetik)
- [2. Mesin Arus Bolak-Balik (AC)](#2-mesin-arus-bolak-balik-ac)
- [3. Mesin Arus Searah (DC)](#3-mesin-arus-searah-dc)
- [4. Transformator (Mesin Statis)](#4-transformator-mesin-statis)

---

## 1. Konsep Dasar Konversi Elektromagnetik

Semua mesin listrik putar (dinamo) bekerja menaati dua prinsip hukum alam utama tentang kemagnetan:

1. **Prinsip Induksi Generator (Hukum Faraday):**  
   *Jika sebuah konduktor/kawat digerakkan menembus garis medan magnet, maka pada kawat tersebut akan timbul Gaya Gerak Listrik (GGL / Tegangan).*
   Inilah alasan mengapa kincir angin yang memutar generator bisa menyalakan lampu (menghasilkan voltase).

2. **Prinsip Tolakan Motor (Hukum Gaya Lorentz):**  
   *Jika sebuah konduktor yang dialiri arus listrik diletakkan melintang di dalam pengaruh medan magnet, konduktor tersebut akan mengalami tolakan (gaya mekanik) yang mendorongnya bergerak.*  
   Ini alasannya mengapa dinamo kipas angin bisa ikut berputar jika kita colokkan ke listrik PLN/Baterai.

---

## 2. Mesin Arus Bolak-Balik (AC)
Ini adalah jenis mesin yang paling dominan digunakan di perindustrian (terutama tipe 3-fasa) karena konstruksinya sangat awet, minim perawatan, serta bisa memakai suplai tegangan besar PLN secara langsung.

### A. Motor AC (Alternating Current Motor)
Terdiri dari dua aliran utama berdasarkan penyesuaian rotasinya:
1. **Motor Induksi (Asinkron):**
   - **Mekanisme:** Dinamakan "induksi" karena belitan poros rotor di tengah tidak dihubungkan langsung menggunakan kabel dari sumber luar, melainkan karena tergugah oleh gelombang *induksi tak kasat mata* dari setruman medan magnet stator yang memutarinya.
   - **Konsep *Slip*:** Ini mutlak! Putaran rotor selalu berlari sedikit lebih lambat mengejar medan putar *stator*. Jika mereka nekat berlari di kecepatan sama mutlak, maka fungsi potong-memotong garis induksi hilang dan motor malah kehilangan torsi (mati perlahan). Perbedaan selisih presentase inilah yang dinamakan **Slip** (kisaran $2\% - 5\%$).
   - **Tipe Utama:** **Sangkar Tupai *(Squirrel Cage)*** yang paling murah dan bandel (bebas sikat/karbon), serta tipe **Rotor Belitan *(Slip-Ring)*** yang butuh disambung resistor luar untuk dorongan *start* yang teramat berat awal.
   
2. **Motor Sinkron:**
   - Spesies ini kecepatan rotornya "terkunci mutlak" sama percis dan berbaris rapi selaras dengan medan arus bolak-balik penggeraknya ($0\%$ slip). Kecepatannya *fix* / konstan di segala beban! (jika ditarik paksa *overload*, dia tidak melambat, namun langsung berhenti / *stall*).
   - Di banyak proyek pabrik, motor jenis ekstra mahal ini tidak dipakai sekedar memutar beban melainkan demi **memperbaiki parameter *Power Factor*/Cosinus Phi daya pabrik** (dimainkan menjadi *Synchronous Condenser*).

### B. Generator AC (Alternator)
- Inilah wujud "Genset Raksasa" pencipta pasokan listrik masif dunia peradaban (PLTA, PLTU).
- **Konstruksi Unik Balik:** Kalau generator DC yang muter itu kawatnya... Pada Alternator raksasa justru dibalik **(Stator / Diam $=$ Rangkaian Kawat Penghasil Listriknya)**, sedangkan **(Rotor / Yang Mutar $=$ Adalah Magnet Penyetrum Bebas)**. Mengapa? Agar hasil panen listrik voltase tingginya bisa langsung dilangsungkan ke kabel tiang listrik tanpa melewati sikat arang komutator berputar yang rawan meledak oleh percikan *arc flash*.

---

## 3. Mesin Arus Searah (DC)
Mesin pengguna listrik baterai ini sangat dihargai karena kepiawaian mutlaknya yaitu **Kepresisian dan kemudahan perputaran Speed Control-nya** dibanding Motor AC, plus torsi angkat mulanya yang ekstrem tangguh. Ciri fisiknya menggunakan mekanisme cincin belah **(Komutator)** dan **Sikat Karbon (Brush)**.

### A. Motor DC
Digolongkan dari bagaimana cara rangkaiannya men-seri/paralelkan medannya:
1. **Motor DC Seri:** Lilitannya seri tegak lurus sejalur. Karakternya? *Starting Torque* super raksasa. Sering dipakai untuk pergerakan tuas Derek Krane, Dinamo Starter Engine Mobil, maupun lokomotif kereta lama. **Peringatan Bahaya:** Mesin tipe DC seri tidak boleh sedetikpun di-dihidupkan kosong blong tanpa *load/beban*, karena putarannya bisa meroket liar tak terkendali (*runaway / overspeed*) sampai dinamonya lepas hancur.
2. **Motor DC Shunt (Paralel):** Karena disusun paralel membentang, kecepatan motor ini sangat stabil meskipun dipaksa menyeret beban mendadak atau dilepas bebannya.
3. **Motor DC Kompon:** Anak blasteran *(Seri + Shunt)*, berusaha memadukan keunggulan keduanya.

### B. Generator DC
- Sebenarnya proses produksi asli listrik di rahim *rotor* selalu berupa gelombang AC. Namun di kepala peluncurnya ditambahkan part krusial bernama cincin belah **Komutator**. 
- Fungsinya persis dioda mekanikal secara sepihak memaksakan menyearahkan gelombang dua arah itu menuju sikat karbon hingga hasilnya keluar sebagai Arus Searah tegangan murni (DC).

---

## 4. Transformator (Trafo / Mesin Statis)
Meskipun tak memiliki suku cadang gir berputar, trafo selalu disertakan di prodi mesin listrik karena ia mengkonversi *transfer* kelistrikan secara magnetal.
- **Goal Mutlak:** Merubah hierarki voltase Arus AC menjadi meninggi tajam *(Step-Up)* atau melantai merendah *(Step-Down)* tanpa mengobrak-abrik sedikitpun struktur frekuensinya (Hz).
- **Cara Kerja:** Terdiri dari kumparan Primer-Sekunder dan teras inti besi. Listrik AC Primer mengirim fluks magnet radiasi melompati jembatan teras besi agar diculik dan melahirkan listrik kembali di sekunder (Induksi mutual).
- **Aturan Rumus Mutlak:** Jika trafonya ideal (efisiensi paripurna 100%), tidak ada yang gratis! Menaikkan Voltase harus dibayar mahal menderita dengan turunnya daya Ampere ($V_p \cdot I_p = V_s \cdot I_s$).

---
[<< 08 - Instrumentasi dan Pengukuran](../08%20-%20Instrumentasi%20dan%20Pengukuran/README.md) | [HOME](../README.md) | [10 - CAD dan CAM >>](../10%20-%20CAD%20dan%20CAM/README.md)
