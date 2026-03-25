# Matematika 2

## Daftar Isi
- [1. Bilangan Imajiner dan Kompleks](#1-bilangan-imajiner-dan-kompleks)
- [2. Vektor, Analisis Vektor, dan Turunan](#2-vektor-analisis-vektor-dan-turunan)
- [3. Referensi: Tabel Sudut Istimewa Trigonometri](#3-referensi-tabel-sudut-istimewa-trigonometri)
- [4. Contoh Soal dan Pembahasan](#4-contoh-soal-dan-pembahasan)

---

## 1. Bilangan Imajiner dan Kompleks

### Sistem Bilangan dan Asal Mula Bilangan Imajinier
Secara garis besar, perwujudan sistem bilangan terbagi dari:
- **Bilangan Real ($\mathbb{R}$):** Gabungan dari rasional (pecahan $a/b$, desimal terbatas) dan irasional ($\pi$, $e$, desimal tak berulang).
- **Bilangan Imajiner/Khayal:** Diperlukan ketika menyelesaikan perhitungan yang tidak terdefinisi dalam bilangan real, seperti akar kuadrat dari bilangan negatif ($\sqrt{-1}$).
- **Bilangan Kompleks:** Gabungan antar bilangan real dan bilangan imajiner.

**Dari mana asalnya?**
Bilangan imajiner muncul terutama dalam penyelesaian akar-akar persamaan kuadrat $ax^2 + bx + c = 0$ menggunakan **Rumus ABC** ketika nilai diskriminannya negatif ($D < 0$):

$$ x_{1,2} = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

*Contoh:* Akar dari $x^2 - 4x + 5 = 0$ memiliki diskriminan $D = (-4)^2 - 4(1)(5) = -4$. Sehingga akarnya adalah $x = \frac{4 \pm \sqrt{-4}}{2} = 2 \pm i$.

Bilangan kompleks terdiri dari bagian real dan bagian imajiner. Bentuk umumnya adalah:

$$ z = a + bi $$

di mana:
- $a =$ bagian real (Re)
- $b =$ bagian imajiner (Im), ($b \neq 0$)
- Jika $a = 0$ dan $b \neq 0$, bilangan disebut **Imajiner murni**.
- $i =$ unit imajiner, dengan definisi $i = \sqrt{-1}$, sehingga $i^2 = -1$.

### Operasi Dasar Bilangan Kompleks
Misalkan $z_1 = a + bi$ dan $z_2 = c + di$:
- **Penjumlahan:** $z_1 + z_2 = (a+c) + (b+d)i$
- **Pengurangan:** $z_1 - z_2 = (a-c) + (b-d)i$
- **Perkalian:** $z_1 \cdot z_2 = (a+bi)(c+di) = (ac - bd) + (ad + bc)i$
- **Pembagian:** Untuk membagi, kalikan sekawan (konjugat) dari penyebut:

$$ \frac{z_1}{z_2} = \frac{a+bi}{c+di} \cdot \frac{c-di}{c-di} = \frac{(ac+bd) + (bc-ad)i}{c^2+d^2} $$

### Bentuk Polar dan Eksponensial (Formula Euler)
Bilangan kompleks juga dapat dinyatakan dalam bentuk polar:

$$ z = r (\cos \theta + i \sin \theta) $$

Dengan Formuler Euler, bentuknya menjadi:

$$ z = r e^{i\theta} $$

di mana:
- Modulus (jarak): $r = |z| = \sqrt{a^2 + b^2}$
- Argumen (sudut): $\theta = \arctan(\frac{b}{a})$

---

## 2. Vektor, Analisis Vektor, dan Turunan

Dalam sistem koordinat maupun penerapannya dalam teknik/elektro, **Skalar** adalah besaran yang hanya memiliki magnitudo (nilai), sedangkan **Vektor** adalah besaran yang memiliki **nilai (magnitude)** dan **arah**. Vektor direpresentasikan dalam bentuk komponen basis unit ($a_x, a_y, a_z$ atau $\hat{i}, \hat{j}, \hat{k}$):

$$ \vec{v} = v_x \hat{i} + v_y \hat{j} + v_z \hat{k} $$

### Vektor Posisi dan Jarak
- **Vektor Posisi:** Vektor yang ditarik dari titik origin/pusat $(0,0,0)$ menuju suatu titik spesifik $P(x,y,z)$.
- **Vektor Jarak:** Pengurangan dua vektor posisi untuk mencari perpindahan antartitik mendefinisikan jarak absolutnya.

### Operasi Dasar Vektor
- **Panjang (Magnitudo):** $|\vec{v}| = \sqrt{v_x^2 + v_y^2 + v_z^2}$
- **Unit Vektor Konstan:** Vektor yang besarnya bernilai satuan $1$, dirumuskan dengan $\hat{u} = \frac{\vec{v}}{|\vec{v}|}$
- **Penjumlahan/Pengurangan:** Dilakukan komponen per komponen.
- **Perkalian Titik (Dot / Scalar Product):** Menghasilkan sebuah *skalar*.

$$ \vec{A} \cdot \vec{B} = A_xB_x + A_yB_y + A_zB_z = |\vec{A}| |\vec{B}| \cos \theta $$

- **Mencari Sudut Antara Dua Vektor:** Dapat dicari menggunakan penjabaran dari rumus Dot Product.

$$ \cos \theta = \frac{\vec{A} \cdot \vec{B}}{|\vec{A}| |\vec{B}|} $$

- **Perkalian Silang (Cross / Vector Product):** Menghasilkan *vektor* baru yang tegak lurus terhadap bidang vektor pembentuknya.

$$ \vec{A} \times \vec{B} = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ A_x & A_y & A_z \\ B_x & B_y & B_z \end{vmatrix} $$

### Turunan Vektor dan Operator Nabla ($\nabla$)
Pendekatan fungsi vektor sering dipakai untuk mencari pergerakan objek dan aliran vektor ruang:
- **Kecepatan dan Percepatan:** Turunan 1 dan 2 dari vektor lintasan. $\vec{v}(t) = \frac{d\vec{r}}{dt}$ dan $\vec{a}(t) = \frac{d\vec{v}}{dt} = \frac{d^2\vec{r}}{dt^2}$

**Kalkulus Vektor Lanjutan:** Operator Nabla / Del ($\nabla$) adalah operator diferensial vektor:

$$ \nabla = \frac{\partial}{\partial x}\hat{i} + \frac{\partial}{\partial y}\hat{j} + \frac{\partial}{\partial z}\hat{k} $$

Aplikasinya digunakan dalam 3 perhitungan kalkulus utama:
1. **Gradien (Gradient):** Operasi $\nabla f$ (Skalar $\to$ Vektor). Digunakan untuk mendapatkan tingkat perubahan maksimum di ruang.
2. **Divergensi (Divergence):** Perkalian Dot $\nabla \cdot \vec{F}$ (Vektor $\to$ Skalar). Menyatakan besarnya sebaran/fluks suatu medan vektor dari suatu titik.
3. **Curl / Rotasi:** Perkalian Cross $\nabla \times \vec{F}$ (Vektor $\to$ Vektor). Mengukur tingkat rotasi atau putaran lintasan vektor. Digunakan pada persamaan Teorema Stokes.

**Aturan Turunan untuk Fungsi Vektor (Waktu):**
1. Turunan penjumlahan: $\frac{d}{dt} [\vec{A}(t) + \vec{B}(t)] = \vec{A}'(t) + \vec{B}'(t)$
2. Turunan perkalian skalar-vektor: $\frac{d}{dt} [u(t)\vec{A}(t)] = u'(t)\vec{A}(t) + u(t)\vec{A}'(t)$
3. Turunan dari Dot Product: $\frac{d}{dt} [\vec{A}(t) \cdot \vec{B}(t)] = \vec{A}'(t)\cdot\vec{B}(t) + \vec{A}(t)\cdot\vec{B}'(t)$
4. Turunan dari Cross Product: $\frac{d}{dt} [\vec{A}(t) \times \vec{B}(t)] = \vec{A}'(t)\times\vec{B}(t) + \vec{A}(t)\times\vec{B}'(t)$

---

## 3. Referensi: Tabel Sudut Istimewa Trigonometri

| Sudut ($\theta$) | Radian ($\pi$) | $\sin \theta$ | $\cos \theta$ | $\tan \theta$ |
| :---: | :---: | :---: | :---: | :---: |
| **$0^\circ$** | $0$ | $0$ | $1$ | $0$ |
| **$30^\circ$** | $\frac{\pi}{6}$ | $\frac{1}{2}$ | $\frac{1}{2}\sqrt{3}$ | $\frac{1}{3}\sqrt{3}$ |
| **$45^\circ$** | $\frac{\pi}{4}$ | $\frac{1}{2}\sqrt{2}$ | $\frac{1}{2}\sqrt{2}$ | $1$ |
| **$60^\circ$** | $\frac{\pi}{3}$ | $\frac{1}{2}\sqrt{3}$ | $\frac{1}{2}$ | $\sqrt{3}$ |
| **$90^\circ$** | $\frac{\pi}{2}$ | $1$ | $0$ | $\infty$ (Tak terdefinisi) |
| **$120^\circ$**| $\frac{2\pi}{3}$ | $\frac{1}{2}\sqrt{3}$ | $-\frac{1}{2}$ | $-\sqrt{3}$ |
| **$135^\circ$**| $\frac{3\pi}{4}$ | $\frac{1}{2}\sqrt{2}$ | $-\frac{1}{2}\sqrt{2}$ | $-1$ |
| **$150^\circ$**| $\frac{5\pi}{6}$ | $\frac{1}{2}$ | $-\frac{1}{2}\sqrt{3}$ | $-\frac{1}{3}\sqrt{3}$ |
| **$180^\circ$**| $\pi$ | $0$ | $-1$ | $0$ |
| **$270^\circ$**| $\frac{3\pi}{2}$ | $-1$ | $0$ | $\infty$ (Tak terdefinisi) |
| **$360^\circ$**| $2\pi$ | $0$ | $1$ | $0$ |

---

## 4. Contoh Soal dan Pembahasan

### Soal 1: Sudut Antara Dua Vektor
Diketahui $\vec{A} = 2\hat{i} + \hat{j} - 2\hat{k}$ dan $\vec{B} = 3\hat{i} - 4\hat{j} + 0\hat{k}$. Tentukan besar sudut antara kedua vektor tersebut!

**Pembahasan:**
1. **Cari nilai perkalian titik (Dot Product):**

$$ \vec{A} \cdot \vec{B} = (2)(3) + (1)(-4) + (-2)(0) = 6 - 4 + 0 = 2 $$

2. **Cari panjang (magnitudo) masing-masing vektor:**

$$ |\vec{A}| = \sqrt{2^2 + 1^2 + (-2)^2} = \sqrt{4+1+4} = \sqrt{9} = 3 $$

$$ |\vec{B}| = \sqrt{3^2 + (-4)^2 + 0^2} = \sqrt{9+16+0} = \sqrt{25} = 5 $$

3. **Masukkan ke rumus sudut:**

$$ \cos \theta = \frac{\vec{A} \cdot \vec{B}}{|\vec{A}| |\vec{B}|} = \frac{2}{3 \times 5} = \frac{2}{15} $$

4. **Hitung besarnya sudut:**

$$ \theta = \arccos\left(\frac{2}{15}\right) \approx 82.34^\circ $$

### Soal 2: Operasi Pembagian Bilangan Kompleks
Jika $z_1 = 3 + 4i$ dan $z_2 = 1 - 2i$, tentukan hasil dari $\frac{z_1}{z_2}$!

**Pembahasan:**
Pecahan untuk pembagian adalah $\frac{3 + 4i}{1 - 2i}$. Untuk memecahkannya, kalikan dengan akar konjugat dari penyebut, yaitu $(1 + 2i)$:

$$ \frac{z_1}{z_2} = \frac{(3+4i)}{(1-2i)} \cdot \frac{(1+2i)}{(1+2i)} $$

Hitung bagian pembilang:

$$ (3+4i)(1+2i) = 3(1) + 3(2i) + 4i(1) + 4i(2i) = 3 + 6i + 4i + 8i^2 $$

Karena $i^2 = -1$, maka pembilang bergeser menjadi:

$$ = 3 + 10i + 8(-1) = 3 + 10i - 8 = -5 + 10i $$

Hitung bagian penyebut:

$$ (1-2i)(1+2i) = 1^2 - (2i)^2 = 1 - 4i^2 = 1 - 4(-1) = 1 + 4 = 5 $$

Gabungkan kembali:

$$ \frac{z_1}{z_2} = \frac{-5 + 10i}{5} = -1 + 2i $$

---
[<< 03 - Praktikum Instrumentasi dan Pengukuran](../03%20-%20Praktikum%20Instrumentasi%20dan%20Pengukuran/README.md) | [HOME](../README.md) | [05 - Bahasa Inggris II >>](../05%20-%20Bahasa%20Inggris%20II/README.md)
