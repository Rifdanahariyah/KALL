---
title: SVD

---

### **SVD (Singular Value Decomposition)**

#### **Apa itu SVD?**

SVD (Singular Value Decomposition) adalah sebuah teknik dalam aljabar linear yang digunakan untuk memecah matriks menjadi tiga matriks yang lebih sederhana. Dalam konteks data, SVD sering digunakan sebagai alat reduksi data atau reduksi dimensionalitas untuk memproses data berukuran besar atau berdimensi tinggi. 


SVD memecah matriks menjadi tiga matriks baru: dua matriks ortogonal (U dan V) dan satu matriks diagonal (Σ). 

$$A = U \Sigma V^{\mathrm{T}}$$

* **$A$**: Matriks yang akan di-dekomposisi. 
* **$U$**: Matriks ortogonal (vektor-vektor singular kiri) $m$ X $n$.
* **$\Sigma$ (sigma)**: Matriks diagonal dengan nilai-nilai singular $m$ X $n$ (akar kuadrat dari nilai eigen matriks $A^{\mathrm{T}} A$.
* **$V^{\mathrm{T}}$**: Transpose dari matriks ortogonal (vektor-vektor singular kanan) $n$ X $n$. 

#### **Kegunaan SVD**

SVD memungkinkan kita untuk memecah matriks menjadi beberapa matriks yang lebih sederhana, yang kemudian dapat digunakan untuk berbagai tujuan seperti kompresi data, reduksi dimensi, dan ekstraksi informasi penting. 

Berikut adalah beberapa kegunaan SVD:

**1. Pengurangan Dimensionalitas**

* Mengurangi jumlah fitur dalam kumpulan data sambil mempertahankan sebagian besar informasi.
* Contoh: Dalam pemrosesan gambar, SVD dapat digunakan untuk mengompresi gambar dengan hanya menyimpan nilai singular yang paling signifikan dan vektor singular yang sesuai. Pendekatan ini, yang dikenal sebagai aproksimasi peringkat rendah, secara signifikan mengurangi ukuran data gambar tanpa kehilangan kualitas yang substansial.

**2. Sistem Rekomendasi**

* Kegunaan: Membangun sistem yang merekomendasikan item (seperti film, buku, produk) kepada pengguna.
* Contoh : SVD dapat digunakan untuk menguraikan matriks penilaian pengguna-item, mengungkap fitur-fitur laten yang mewakili preferensi pengguna dan karakteristik item yang mendasarinya. Fitur-fitur ini kemudian dapat digunakan untuk memprediksi penilaian yang hilang dan merekomendasikan item kepada pengguna.

**3. Pemrosesan Bahasa Alami (NLP)**

* Kegunaan : Mengidentifikasi pola dalam data teks, seperti pemodelan topik.
* Contoh : Dalam pemodelan topik untuk sekumpulan dokumen, SVD dapat menguraikan matriks istilah-dokumen untuk mengidentifikasi topik-topik laten. Setiap topik merupakan gabungan dari istilah-istilah, dan setiap dokumen merupakan campuran dari topik-topik ini, yang membantu dalam mengkategorikan dan meringkas kumpulan besar data teks.

**4. Pemrosesan Sinyal**

* Kegunaan : Pengurangan kebisingan dan penyaringan sinyal.
* Contoh : Dalam pemrosesan sinyal audio, SVD dapat digunakan untuk memisahkan noise dari sinyal sebenarnya. Dengan menguraikan matriks sinyal dan membuang komponen dengan nilai singular rendah (yang sering kali merupakan noise), kualitas sinyal audio dapat ditingkatkan.

**5. Pengolahan Gambar**

* Kegunaan : Ekstraksi fitur dan pengenalan gambar.
* Contoh : Dalam sistem pengenalan wajah, SVD dapat membantu mengekstraksi fitur-fitur penting dari gambar wajah. Dengan memecah data gambar menjadi nilai-nilai tunggal dan vektor, sistem dapat berfokus pada fitur-fitur pengenalan wajah yang paling informatif.

---

#### **Contoh 1:**

Matriks: 

$$
A = \begin{bmatrix}
3 & 1 \\
1 & 3
\end{bmatrix}
$$

* **Hitung $A^{\mathrm{T}} A$**

karena $A$ adalah matriks simetris, maka:

$$
A = A^{\mathrm{T}} = \begin{bmatrix}
3 & 1 \\
1 & 3
\end{bmatrix}
$$

Maka:

$$
A^{\mathrm{T}} = A \quad
= \begin{bmatrix}
3 & 1 \\
1 & 3
\end{bmatrix} \quad
$$

$$
A^{\mathrm{T}}A = A \cdot A =
\begin{bmatrix}
3 & 1 \\
1 & 3
\end{bmatrix}
\begin{bmatrix}
3 & 1 \\
1 & 3
\end{bmatrix}
= \begin{bmatrix}
3\cdot3 + 1\cdot1 & 3\cdot1 + 1\cdot3 \\
1\cdot3 + 3\cdot1 & 1\cdot1 + 3\cdot3
\end{bmatrix}
= \begin{bmatrix}
10 & 6 \\
6 & 10
\end{bmatrix}
$$

* **Mencari Eigenvalues**

diketahui:

$$ A^{\mathrm{T}} A = \begin{bmatrix} 10 & 6 \\ 6 & 10 \end{bmatrix}
$$

$$
\det(A - \lambda I) = 
\left| 
\begin{array}{cc}
10 - \lambda & 6 \\
6 & 10 - \lambda
\end{array}
\right|
= (10 - \lambda)^2 - 6^2 = 0
$$

$$
(10 - \lambda)^2 - 36 = 0
\Rightarrow (10 - \lambda)^2 = 36
\Rightarrow 10 - \lambda = \pm 6
$$

$$
\Rightarrow
\begin{cases}
\lambda_1 = 10 + 6 = 16 \\
\lambda_2 = 10 - 6 = 4
\end{cases}
$$

$$
\lambda_1 = 16, \quad \lambda_2 = 4
$$

* **Hitung Singular Values**

$$\sigma_1 = \sqrt{16} = 4, \quad \sigma_2 = \sqrt{4} = 2$$

* **Mencari Eigenvector**

Untuk $\lambda = 16:$

$$
( A^{T}A - 16I ) = 
\begin{bmatrix}
-6 & 6 \\
6 & -6
\end{bmatrix}
\cdot
\begin{bmatrix}
x \\
y
\end{bmatrix}
= 0
\Rightarrow -6x + 6y = 0 \Rightarrow x = y
$$

$$
\vec{v}_1 = 
\begin{bmatrix}
1 \\
1
\end{bmatrix}
\Rightarrow 
\frac{1}{\sqrt{2}} 
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

Untuk $\lambda = 4:$

$$
(A - 4I)\vec{v} = 0 \Rightarrow
\begin{bmatrix}
6 & 6 \\
6 & 6
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
= \begin{bmatrix}
0 \\
0
\end{bmatrix}
\Rightarrow 6x + 6y = 0 \Rightarrow x = -y
$$

$$
\vec{v}_2 = 
\begin{bmatrix}
1 \\
-1
\end{bmatrix}
\Rightarrow
\frac{1}{\sqrt{2}} 
\begin{bmatrix}
1 \\
-1
\end{bmatrix}
$$

Maka:

$$V = 
\begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}
\end{bmatrix}$$

* **Hitung $U$ dengan rumus**

$$
\vec{u}_i = \frac{1}{\sigma_i} A \mathbf{v}_i
$$

Untuk: $\sigma_1 = 4 \), \( \vec{v}_1 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix}$

$$
\vec{u}_1 = \frac{1}{4} A \vec{v}_1 = \frac{1}{4} A \cdot \frac{1}{\sqrt{2}} 
\begin{bmatrix}
1 \\
1
\end{bmatrix}
= \frac{1}{4\sqrt{2}} 
\begin{bmatrix}
3 + 1 \\
1 + 3
\end{bmatrix}
= \frac{1}{\sqrt{2}} 
\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

Untuk: $\sigma_2 = 2 \), \( \vec{v}_2 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ -1 \end{bmatrix}$  

$$
\vec{u}_2 = \frac{1}{2} A \vec{v}_2 = \frac{1}{2} A \cdot \frac{1}{\sqrt{2}} 
\begin{bmatrix}
1 \\
-1
\end{bmatrix}
= \frac{1}{2\sqrt{2}} 
\begin{bmatrix}
3 - 1 \\
1 - 3
\end{bmatrix}
= \frac{1}{\sqrt{2}} 
\begin{bmatrix}
1 \\
-1
\end{bmatrix}
$$

Maka:

$$
U = 
\begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}
\end{bmatrix}
$$

* **Matriks $\Sigma$**

$$\Sigma = 
\begin{bmatrix}
4 & 0 \\
0 & 2
\end{bmatrix}$$

Maka:

$$A = U \Sigma V^T$$

Dengan:

$$
U = 
\begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}
\end{bmatrix},
\quad
\Sigma = 
\begin{bmatrix}
4 & 0 \\
0 & 2
\end{bmatrix},
\quad
V = 
\begin{bmatrix}
\frac{1}{\sqrt{2}} & \frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{2}}
\end{bmatrix}
$$



---

#### **Contoh 2:**

Misalnya:

$$
A = \begin{bmatrix}
4 & 1 \\
2 & 7 \\
1 & 4 
\end{bmatrix}
$$

* **Hitung $A^{\mathrm{T}} A$**

$$
A^{\mathrm{T}}
= \begin{bmatrix}
4 & 2 & 1\\
1 & 7 & 4
\end{bmatrix} \quad
$$

Maka:

$$
A^T A = 
\begin{bmatrix}
4 & 2 & 1\\
1 & 7 & 4 
\end{bmatrix}
\cdot
\begin{bmatrix}
4 & 1 \\
2 & 7 \\
1 & 4
\end{bmatrix}
$$

$$
A^T A = 
\begin{bmatrix}
(4^2 + 2^2 + 1^2) & (4 \cdot 1 + 2 \cdot 7 + 1 \cdot 4) \\
(1 \cdot 4 + 7 \cdot 2 + 4 \cdot 1) & (1^2 + 7^2 + 4^2)
\end{bmatrix}
=\begin{bmatrix}
21 & 26 \\
26 & 66
\end{bmatrix}
$$

* **Mencari Eigenvalues dari $A^T A$**

$$
\det(A^T A - \lambda I) = \lambda^2 - 87\lambda + 1025 = 0
$$

Hasil dari persamaan kuadrat tersebut:

$$
\lambda_1 \approx 72.5, \quad \lambda_2 \approx 14.6
$$

Sehingga, nilai singular values (akar dari eigenvalue matriks $( A^T A)$ adalah:

$$
\sigma_1 = \sqrt{\lambda_1} \approx \sqrt{72.5} \approx 8.51
$$

$$
\sigma_2 = \sqrt{\lambda_2} \approx \sqrt{14.6} \approx 3.82
$$

* **Mencari Eigenvector $v_1$ dan $v_2$ untuk $A^T A$** 

Untuk $\lambda_1 = 72.5$:

$$
(A^T A - \lambda I) \vec{v} = 0 \Rightarrow \vec{v}_1=
\begin{bmatrix}
0.316 \\
0.949
\end{bmatrix}
$$

Untuk $\lambda_2 = 14.6$:

$$
\vec{v}_2 =
\begin{bmatrix}
0.949 \\
-0.316
\end{bmatrix}
$$

Sehingga matriks $V^T$ (transpose dari matriks eigenvektor-ortonormal $V$  adalah:

$$
V^T = 
\begin{bmatrix}
0.316 & 0.949 \\
0.949 & -0.316
\end{bmatrix}
$$

* **Hitung $U$ dengan rumus:**

$$\vec{u}_i = \frac{1}{\sigma_i} A \vec{v}_i$$

Misalnya:

$$
A 
\begin{bmatrix}
0.316 \\
0.949
\end{bmatrix}
=\begin{bmatrix}
2.669 \\
5.705 \\
5.111
\end{bmatrix}
\Rightarrow
\vec{u}_1 = \frac{1}{8.51}
\begin{bmatrix}
2.669 \\
5.705 \\
5.111
\end{bmatrix}
\approx
\begin{bmatrix}
0.43 \\
0.67 \\
0.60
\end{bmatrix}
$$

Begitu juga untuk vektor ortonormal kedua:

$$
\vec{u}_2 \approx 
\begin{bmatrix}
-0.56 \\
0.43 \\
-0.70
\end{bmatrix}
$$

* **Matriks $\Sigma$**

$$
\Sigma = 
\begin{bmatrix}
8.51 & 0 & 0 \\
0 & 3.82 & 0 
\end{bmatrix}
$$

Maka:

Dekomposisi SVD dari matriks $A$ dalam bentuk $A = U \Sigma V^T$ adalah:

$$
U \approx 
\begin{bmatrix}
0.43 & 0.67 & 0.60 \\
-0.56 & 0.43 & -0.70 \\
u_{31} & u_{32} & u_{33}
\end{bmatrix}, \quad
\Sigma = 
\begin{bmatrix}
8.51 & 0 & 0 \\
0 & 3.82 & 0 
\end{bmatrix}, \quad
V^T = 
\begin{bmatrix}
0.316 & 0.949 \\
0.949 & -0.316
\end{bmatrix}
$$