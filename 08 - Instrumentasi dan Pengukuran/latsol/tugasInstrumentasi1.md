# Tugas Instrumentasi dan Pengukuran 1

## 1. Susunan Instrumentasi Secara Umum

Secara umum, sistem instrumentasi terdiri dari blok fungsional yang bekerja berurutan untuk mengubah besaran fisik menjadi data digital yang dapat dibaca pengguna.

1. **Besaran Fisis**: Variabel alam yang diukur (input), pada tugas ini berupa **suhu**.
2. **Sensor**: Komponen yang mendeteksi perubahan besaran fisik dan mengubahnya menjadi sinyal listrik.
3. **Pengkondisi Sinyal**: Penguat atau penyaring sinyal agar sesuai untuk tahap konversi.
4. **ADC (Analog-to-Digital Converter)**: Mengubah sinyal analog menjadi data digital.
5. **Pemroses**: Mengolah data digital menjadi nilai temperatur menggunakan persamaan yang sesuai.
6. **Penampil**: Menyajikan hasil pengukuran kepada pengguna.

### Contoh Jalur Komponen Instrumentasi Suhu

| Tahapan | Jalur Sensor LM35 | Jalur Sensor Termistor |
| :--- | :--- | :--- |
| **Besaran Fisis** | Suhu ($17^\circ C$) | Suhu ($^\circ C$) |
| **Sensor** | LM35 | Termistor |
| **Pengkondisi Sinyal** | Op-amp ($V_o = 10V_i$) | Rangkaian pembagi tegangan |
| **ADC** | ADC 8-bit | ADC 8-bit |
| **Pemroses** | Persamaan linier | Persamaan eksponensial |
| **Penampil** | Suhu ($^\circ C$) | Suhu ($^\circ C$) |

---

## 2. Analisis Data Eksperimen

Data hasil eksperimen untuk kedua sensor adalah sebagai berikut.

| Suhu ($^\circ C$) | LM35 (V) | Termistor ($\Omega$) |
| :---: | :---: | :---: |
| 0 | 0.0 | 20 |
| 10 | 0.1 | 55 |
| 20 | 0.2 | 150 |
| 30 | 0.3 | 400 |
| 40 | 0.4 | 1100 |
| 50 | 0.5 | 3000 |

**Analisis singkat:**

1. **LM35** menunjukkan respons linier sempurna sebesar $10\text{ mV}/^\circ C$.
2. **Termistor** menunjukkan respons nonlinier (eksponensial), terlihat dari kenaikan hambatan yang semakin besar saat suhu naik.

### Analisis Lanjutan

#### A. Respons Sensor LM35

1. Jika suhu naik sebesar $10^\circ C$, maka tegangan LM35 naik sebesar $0.1V$.
2. Jika suhu naik dua kali lipat, maka tegangan keluaran LM35 juga naik dua kali lipat.
3. Jika suhu berubah kecil (misalnya $1^\circ C$), maka perubahan tegangan juga kecil dan tetap proporsional ($0.01V$).
4. Jika grafik suhu terhadap tegangan digambar, maka bentuk grafik berupa garis lurus (linier).

Ringkasan numerik dari tabel LM35:

- $0^\circ C \to 0.0V$
- $10^\circ C \to 0.1V$
- $20^\circ C \to 0.2V$
- $30^\circ C \to 0.3V$
- $40^\circ C \to 0.4V$
- $50^\circ C \to 0.5V$

Kenaikan per langkah suhu konstan, yaitu $\Delta V = +0.1V$ tiap $\Delta T = +10^\circ C$.

#### B. Respons Sensor Termistor

1. Jika suhu naik, maka hambatan termistor juga naik, tetapi tidak dengan selisih yang tetap.
2. Jika suhu berada di rentang rendah, maka kenaikan hambatan masih relatif kecil.
3. Jika suhu berada di rentang tinggi, maka kenaikan hambatan menjadi sangat besar.
4. Jika grafik suhu terhadap hambatan digambar, maka grafik melengkung (nonlinier/eksponensial).

Ringkasan kenaikan hambatan per $10^\circ C$ dari tabel:

- $0 \to 10^\circ C$: $20 \to 55\Omega$ (naik $35\Omega$)
- $10 \to 20^\circ C$: $55 \to 150\Omega$ (naik $95\Omega$)
- $20 \to 30^\circ C$: $150 \to 400\Omega$ (naik $250\Omega$)
- $30 \to 40^\circ C$: $400 \to 1100\Omega$ (naik $700\Omega$)
- $40 \to 50^\circ C$: $1100 \to 3000\Omega$ (naik $1900\Omega$)

Kenaikan per langkah suhu semakin besar, sehingga sensitivitas termistor terhadap suhu menjadi makin tinggi pada suhu yang lebih tinggi.

#### C. Implikasi Praktis

1. Jika dibutuhkan perhitungan sederhana dan cepat, maka LM35 lebih mudah karena relasinya linier.
2. Jika dibutuhkan kepekaan lebih tinggi pada rentang suhu tertentu, maka termistor dapat lebih sensitif, tetapi perlu kalibrasi/persamaan nonlinier.
3. Jika sistem memakai ADC, maka sinyal termistor biasanya memerlukan pemrosesan tambahan agar konversi suhu akurat di seluruh rentang.

---

## 3. Materi Pengkondisi Sinyal

### A. Sensor LM35 (Op-amp CA3140)

Konfigurasi op-amp digunakan untuk menaikkan level tegangan keluaran sensor.

- Rumus umum:

$$
V_o = \frac{R_2}{R_1} V_i
$$

- Implementasi pada tugas (penguatan 10x):

$$
V_o = 10V_i
$$

### B. Sensor Termistor (Pembagi Tegangan)

Rangkaian pembagi tegangan digunakan untuk mengubah perubahan hambatan termistor menjadi tegangan.

- Rumus umum:

$$
V_o = \frac{R_{TH}}{R_{TH} + R} \cdot V_i
$$

- Implementasi pada tugas:

$$
V_o = \frac{R_{TH}}{R_{TH} + 1k\Omega} \cdot 5
$$