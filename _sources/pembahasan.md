---

### **Penyelesaian Sistem Persamaan Linear 3 Variabel dengan Eliminasi Gauss**
Sebuah sistem persamaan linear dengan 3 variabel bisa memiliki:
1. **Satu solusi unik** (sistem konsisten dan determinan matriks koefisien tidak nol).
2. **Tak hingga banyak solusi** (sistem konsisten tetapi terdapat variabel bebas).
3. **Tanpa solusi** (sistem tidak konsisten, terjadi kontradiksi).

Kita akan melihat bagaimana Eliminasi Gauss membantu menentukan jenis solusi.

---

## **1. Contoh Sistem dengan Satu Solusi Unik**
Misalkan sistem persamaan:
$$
\begin{aligned}
2x + y + z &= 9 \\
4x + 3y + 2z &= 24 \\
6x + 5y + 4z &= 42
\end{aligned}
$$

**Langkah 1: Tulis dalam bentuk matriks augmented**
$$
\begin{bmatrix}
2 & 1 & 1 & | 9 \\
4 & 3 & 2 & | 24 \\
6 & 5 & 4 & | 42
\end{bmatrix}
$$

**Langkah 2: Ubah elemen pivot pertama menjadi 1** (bagi baris pertama dengan 2)
$$
\begin{bmatrix}
1 & 0.5 & 0.5 & | 4.5 \\
4 & 3 & 2 & | 24 \\
6 & 5 & 4 & | 42
\end{bmatrix}
$$

**Langkah 3: Nolkan elemen di bawah pivot pertama**
$$
\begin{align*}
R_2 &\to R_2 - 4R_1 \\
R_3 &\to R_3 - 6R_1
\end{align*}
$$

$$
\begin{bmatrix}
1 & 0.5 & 0.5 & | 4.5 \\
0 & 1 & 0 & | 6 \\
0 & 2 & 1 & | 15
\end{bmatrix}
$$

**Langkah 4: Nolkan elemen di bawah pivot kedua**
$$
\begin{align*}
R_3 &\to R_3 - 2R_2
\end{align*}
$$

$$
\begin{bmatrix}
1 & 0.5 & 0.5 & | 4.5 \\
0 & 1 & 0 & | 6 \\
0 & 0 & 1 & | 3
\end{bmatrix}
$$

**Langkah 5: Substitusi balik**
- \( z = 3 \)
- \( y = 6 \)
- $( x + 0.5(6) + 0.5(3) = 4.5 \Rightarrow x = 0 )$

**Kesimpulan:** \( (x, y, z) = (0,6,3) \) adalah **solusi unik**.

<iframe src="https://www.geogebra.org/3d/ehvxgmkw"
width="800" height="600" style="border:0;"></iframe>
        

---

## **2. Contoh Sistem dengan Tak Hingga Banyak Solusi**
Misalkan sistem:
$$
\begin{aligned}
x + y + z &= 6 \\
2x + 2y + 2z &= 12 \\
3x + 3y + 3z &= 18
\end{aligned}
$$

**Langkah 1: Tulis dalam bentuk matriks augmented**
$$
\begin{bmatrix}
1 & 1 & 1 & | 6 \\
2 & 2 & 2 & | 12 \\
3 & 3 & 3 & | 18
\end{bmatrix}
$$

**Langkah 2: Nolkan elemen di bawah pivot pertama**
$$
\begin{aligned}
R_2 &\rightarrow R_2 - 2R_1 \\
R_3 &\rightarrow R_3 - 3R_1
\end{aligned}
$$

$$
\begin{bmatrix}
1 & 1 & 1 & | 6 \\
0 & 0 & 0 & | 0 \\
0 & 0 & 0 & | 0
\end{bmatrix}
$$

**Langkah 3: Interpretasi Hasil**
- Baris kedua dan ketiga hanya berisi nol, sehingga ada **variabel bebas**.
- Kita bisa menulis:
  - \( x + y + z = 6 \)
  - Pilih  z = t , maka y = 6 - x - t 


**Kesimpulan:** Sistem memiliki **tak hingga banyak solusi**, karena terdapat **satu variabel bebas**.

<iframe src="https://www.geogebra.org/3d/mu9nbhn9"
width="800" height="600" style="border:0;"></iframe>

---

## **3. Contoh Sistem dengan Tanpa Solusi**
Mari kita analisis sistem persamaan linear yang diberikan:
$$
\begin{aligned}
x + y + z &= 3 \\
2x + 2y + 2z &= 10 \\
2x + 2y + 2z &= 15
\end{aligned}
$$

### **Langkah 1: Representasi Matriks Augmented**
Kita bisa menuliskan sistem ini dalam bentuk matriks:
$$
\begin{bmatrix} 
1 & 1 & 1 & | 3 \\ 
2 & 2 & 2 & | 10 \\ 
2 & 2 & 2 & | 15 
\end{bmatrix}
$$

### **Langkah 2: Eliminasi Gauss**
- Baris 2 → Baris 2 - 2 × Baris 1  
- Baris 3 → Baris 3 - 2 × Baris 1  

Maka:

$$
\begin{bmatrix} 
1 & 1 & 1 & | 3 \\ 
0 & 0 & 0 & | 4 \\ 
0 & 0 & 0 & | 9 
\end{bmatrix}
$$

### **Langkah 3: Analisis Hasil**
Baris kedua dan ketiga menghasilkan:
$$
0 = 4 \quad \text{(kontradiksi)}
\]
\[
0 = 9 \quad \text{(kontradiksi)}
$$

Pernyataan ini **tidak mungkin benar**, sehingga sistem persamaan ini **tidak memiliki solusi** (inkonsisten).  

### **Kesimpulan**
Sistem ini **tidak memiliki solusi** karena baris terakhir mengandung pertidaksamaan yang mustahil (\(0 = 9\)). Artinya, tidak ada nilai \( x, y, z \) yang dapat memenuhi semua persamaan sekaligus.

<iframe src="https://www.geogebra.org/3d/y6ywzpq5"width="800" height="600" style="border:0;"></iframe>

---

## **Kesimpulan Umum**
- **Satu solusi unik** terjadi jika setelah eliminasi Gauss, matriks menjadi **segitiga atas dengan diagonal utama tidak nol**.
- **Tak hingga banyak solusi** terjadi jika terdapat **variabel bebas** dalam matriks yang menghasilkan satu atau lebih parameter bebas.
- **Tanpa solusi** terjadi jika ada **baris dengan semua elemen nol tetapi nilai konstanta tidak nol**, yang berarti ada kontradiksi dalam sistem.

