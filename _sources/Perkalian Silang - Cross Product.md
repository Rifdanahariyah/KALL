---
title: Perkalian Silang - Cross Product

---

### **Perkalian Silang (Cross Product)**

#### **Definisi Perkalian Silang**
Misalkan:

$$
\vec{u} = \begin{bmatrix}
u_1 \\
u_2 \\
u_3
\end{bmatrix}, \quad
\vec{v} = \begin{bmatrix}
v_1 \\
v_2 \\
v_3
\end{bmatrix}
$$

adalah vektor-vektor di $\mathbb{R}^3$. Hasil kali silang dari $\vec{u}$ dan $\vec{v}$, dinotasikan sebagai $\vec{u} \times \vec{v}$, adalah vektor:

$$
\vec{u} \times \vec{v} = \begin{bmatrix}
u_2 v_3 - u_3 v_2 \\
-(u_1 v_3 - u_3 v_1) \\
u_1 v_2 - u_2 v_1
\end{bmatrix}.
$$

#### **Contoh Menghitung Hasil Kali Silang**

Misalkan:

$$
\vec{u} = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}, \quad
\vec{v} = \begin{bmatrix} 4 \\ 0 \\ -1 \end{bmatrix}
$$

  * ##### **Hitung Kali Silang** $\vec{u} \times \vec{v}$
  
$$
\vec{u} \times \vec{v} =
\begin{bmatrix}
(2)(-1) - (3)(0) \\
-((1)(-1) - (3)(4)) \\
(1)(0) - (2)(4)
\end{bmatrix}
= \begin{bmatrix}
-2 \\
-(-1 - 12) \\
0 - 8
\end{bmatrix}
=\begin{bmatrix}
-2 \\
13 \\
-8
\end{bmatrix}
$$

* ##### **Identifikasi Tegak Lurus pada**  $\vec{u}$

$$
(\vec{u} \times \vec{v}) \cdot \vec{u} =
\begin{bmatrix} -2 \\ 13 \\ -8 \end{bmatrix} \cdot
\begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}
= (-2)(1) + (13)(2) + (-8)(3) = -2 + 26 - 24 = 0
$$

* ##### **Identifikasi Tegak Lurus pada** $\vec{v}$

$$
(\vec{u} \times \vec{v}) \cdot \vec{v} =
\begin{bmatrix} -2 \\ 13 \\ -8 \end{bmatrix} \cdot
\begin{bmatrix} 4 \\ 0 \\ -1 \end{bmatrix}
= (-2)(4) + (13)(0) + (-8)(-1) = -8 + 0 + 8 = 0
$$

Karena $(\vec{u} \times \vec{v}) \cdot \vec{u} = 0$ dan $(\vec{u} \times \vec{v}) \cdot \vec{v} = 0$, maka $(\vec{u} \times \vec{v})$ tegak lurus terhadap $(\vec{u})$ maupun $(\vec{v})$.

---

#### **Menggunakan determinan untuk menemukan perkalian silang**

Membentuk array $3 \times 3$ seperti yang ditunjukkan di bawah ini.

$$
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
u_1 & u_2 & u_3 \\
v_1 & v_2 & v_3
\end{vmatrix}
$$

$$
\vec{u} \times \vec{v} =
\begin{vmatrix}
u_2 & u_3 \\
v_2 & v_3
\end{vmatrix}
\vec{i}
-\begin{vmatrix}
u_1 & u_3 \\
v_1 & v_3
\end{vmatrix} \vec{j}
+\begin{vmatrix}
u_1 & u_2 \\
v_1 & v_2
\end{vmatrix} \vec{k}
$$

$$
\vec{u} \times \vec{v} = (u_2v_3 - u_3v_2)\vec{i} - (u_1v_3 - u_3v_1)\vec{j} + (u_1v_2 - u_2v_1)\vec{k}
$$

##### **Perkalian Silang Vektor**

$$
\vec{v} \times \vec{u} = \det
\begin{bmatrix}
\vec{i} & \vec{j} & \vec{k} \\
v_1 & v_2 & v_3 \\
u_1 & u_2 & u_3
\end{bmatrix}
$$

$$
\left|
\begin{array}{cc}
v_2 & v_3 \\
u_2 & u_3
\end{array} \right| \vec{i} -
\left|
\begin{array}{cc}
v_1 & v_3 \\
u_1 & u_3
\end{array}
\right| \vec{j} +
\left|
\begin{array}{cc}
v_1 & v_2 \\
u_1 & u_2
\end{array}
\right| \vec{k}
= (v_2 u_3 - v_3 u_2) \vec{i} - (v_1 u_3 - v_3 u_1) \vec{j} + (v_1 u_2 - v_2 u_1) \vec{k}
$$

$$
\vec{v} \times \vec{u} =
\begin{bmatrix}
v_2 u_3 - v_3 u_2 \\
-(v_1 u_3 - v_3 u_1) \\
v_1 u_2 - v_2 u_1
\end{bmatrix}
$$

##### **Contoh 1**

Misalkan:

Vektor dari Titik-Titik

Titik $A = (0, 0, 0)$ → Titik pangkal semua vektor

* Titik $C = (1, 1, 1)$ → Maka:
$$\vec{v} = \vec{AC} = 
\begin{pmatrix}
1 \\
1 \\
1\end{pmatrix}
$$

* Titik $D = (1, 0, 0)$ → Maka:
$$\vec{w} = \vec{AD} = 
\begin{pmatrix}
1 \\
0 \\
0
\end{pmatrix}
$$

* Titik $E = (0, 1, 0)$ → Maka:
$$ \vec{a} = \vec{AE} = \begin{pmatrix}
0 \\
1 \\
0
\end{pmatrix}
$$

Menghitung hasil perkalian silang menggunakan determinan matriks:

$$
\vec{w} = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}, \quad
\vec{a} = \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix}
$$

$$
\vec{w} \times \vec{a} = 
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
1 & 0 & 0 \\
0 & 1 & 0 \\
\end{vmatrix}
$$

$$
\left| 
\begin{matrix}
0 & 0 \\
1 & 0
\end{matrix}
\right|
= (0)(0) - (1)(0) = 0 \quad \Rightarrow \quad 0\vec{i}
$$

$$
\left| 
\begin{matrix}
1 & 0 \\
0 & 0
\end{matrix}
\right|
= (1)(0) - (0)(0) = 0 \quad \Rightarrow \quad -0\vec{j}
$$

$$
\left| 
\begin{matrix}
1 & 0 \\
0 & 1
\end{matrix}
\right|
= (1)(1) - (0)(0) = 1 \quad \Rightarrow \quad 1\vec{k}
$$

Hasil akhir:
$$
\vec{w} \times \vec{a} = 
\begin{pmatrix}
0 \\
0 \\
1
\end{pmatrix}
$$

<iframe src="https://www.geogebra.org/classic/tyfxuyuc" width="800" height="600" style="border:0;"></iframe>

##### **Contoh 2**

* $A = (0, 0, 0)$ → Titik pangkal semua vektor
* $B = (1, 1, 1)$, maka vektor:
$$\vec{u} = \vec{AB} = \begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix}$$
* $C = (2, 1, 1)$, maka vektor:
$$\vec{v} = \vec{AC} = \begin{pmatrix} 2 \\ 1 \\ 1 \end{pmatrix}$$
* $D = (0, 0, -1)$, maka vektor:
$$\vec{w} = \vec{AD} = \begin{pmatrix} 0 \\ 0 \\ -1 \end{pmatrix}$$

Perkalian Silang $(\vec{u} \times \vec{v})$

Untuk mendapatkan vektor normal dari bidang yang dibentuk oleh $\vec{u}$ dan $\vec{v}$:

$$
\vec{u} \times \vec{v} = 
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
1 & 1 & 1 \\
2 & 1 & 1
\end{vmatrix}
$$

Komponen-komponennya adalah:

$$\begin{align*}
\quad 
\begin{vmatrix}
1 & 1 \\
1 & 1
\end{vmatrix}
= (1)(1) - (1)(1) = 0 \Rightarrow 0\vec{i} \\
\quad 
\begin{vmatrix}
1 & 1 \\
2 & 1
\end{vmatrix}
= (1)(1) - (1)(2) = -1 \Rightarrow -(-1)\vec{j} = +1\vec{j} \\
\quad 
\begin{vmatrix}
1 & 1 \\
2 & 1
\end{vmatrix}
= (1)(1) - (1)(2) = -1 \Rightarrow -1\vec{k}
\end{align*}
$$

Hasil Akhir:

$$
\vec{u} \times \vec{v} = 0\vec{i} + 1\vec{j} - 1\vec{k} = \begin{pmatrix} 0 \\ 1 \\ -1 \end{pmatrix}
$$

<iframe src="https://www.geogebra.org/classic/fxxyttdk" width="800" height="600" style="border:0;"></iframe>

---

#### **Sifat-sifat Perkalian Silang**

1. Antikomutatif

$$
\mathbf{u} \times \mathbf{v} = -(\mathbf{v} \times \mathbf{u})
$$

2. Distributif terhadap Penjumlahan 

$$
a.(\mathbf{u} + \mathbf{v}) \times \mathbf{w} = \mathbf{u} \times \mathbf{w} + \mathbf{v} \times \mathbf{w}
$$

$$
b. \mathbf{u} \times (\mathbf{v} + \mathbf{w}) = \mathbf{u} \times \mathbf{v} + \mathbf{u} \times \mathbf{w}
$$

3. Konsistensi dengan Perkalian Skalar

$$
c(\mathbf{u} \times \mathbf{v}) = (c\mathbf{u}) \times \mathbf{v} = \mathbf{u} \times (c\mathbf{v})
$$

4. Ortogonal terhadap Faktor 
  
$$
a.(\mathbf{u} \times \mathbf{v}) \cdot \mathbf{u} = 0
$$

$$
b. (\mathbf{u} \times \mathbf{v}) \cdot \mathbf{v} = 0
$$
   
5. Cross Product Vektor dengan Dirinya Sendiri

$$
\mathbf{u} \times \mathbf{u} = \mathbf{0}
$$

6. Cross Product Nol 

$$
\mathbf{0} \times \mathbf{0} = \mathbf{0}
$$

7. Triple Scalar Product

$$
\mathbf{u} \cdot (\mathbf{v} \times \mathbf{w}) = \mathbf{v} \cdot (\mathbf{w} \times \mathbf{u}) = \mathbf{w} \cdot (\mathbf{u} \times \mathbf{v})
$$

#### **Hasil Kali Silang dan Sudut**

Misalkan $\mathbf{u}$ dan $\mathbf{v}$ adalah vektor tak nol di $\mathbb{R}^3$. Maka

$$
\|\mathbf{u} \times \mathbf{v}\| = \|\mathbf{u}\| \, \|\mathbf{v}\| \sin(\theta),
$$

di mana $0 \leq \theta \leq \pi$ adalah sudut antara $\mathbf{u}$ dan $\mathbf{v}$.

---

#### **Implementasi Luas Jajargenjang**

Secara geometris, luas jajar genjang adalah $𝐴 = 𝑏.h$ di mana $b$ adalah panjang alas dan $h$ adalah tinggi jajar genjang. Dalam ruang tiga dimensi, kita bisa menghitung luas jajar genjang yang dibentuk oleh dua vektor menggunakan aturan jajar genjang penjumlahan vektor.

Dari gambar 3D yang Anda berikan, diketahui dua vektor:
$$
\vec{u} = 
\begin{pmatrix}
2 \\
4 \\
0
\end{pmatrix}, \quad
\vec{v} = 
\begin{pmatrix}
-3 \\
3 \\
0
\end{pmatrix}
$$

yang berasal dari titik $A$ sebagai titik pangkal dan membentuk jajar genjang seperti yang terlihat pada bidang
Tinggi jajar genjang dapat dinyatakan sebagai:

$$
h = \|\vec{u}\| \sin(\theta)
$$

Sehingga, luas jajaran genjang yang dibentuk oleh $\vec{u}$ dan $\vec{v}$ adalah:

$$
A = \|\vec{u}\| \|\vec{v}\| \sin(\theta) = \|\vec{u} \times \vec{v}\|
$$

Diketahui:

$$
\vec{u} = 
\begin{pmatrix}
2 \\
4 \\
0
\end{pmatrix}, \quad
\vec{v} = 
\begin{pmatrix}
-3 \\
3 \\
0
\end{pmatrix}
$$

Hitung perkalian silang:

$$
\vec{u} \times \vec{v} = 
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
2 & 4 & 0 \\
-3 & 3 & 0
\end{vmatrix}= \vec{i}(4 \cdot 0 - 0 \cdot 3)- \vec{j}(2 \cdot 0 - 0 \cdot (-3))+ \vec{k}(2 \cdot 3 - (-3) \cdot 4)
$$

Panjang dari $\vec{u} \times \vec{v}$ adalah:

$$
\|\vec{u} \times \vec{v}\| = \sqrt{0^2 + 0^2 + 18^2} = \sqrt{324} = 18
$$

<iframe src="https://www.geogebra.org/classic/s25wajyg" width="800" height="600" style="border:0;"></iframe>

---

#### **Tugas**

##### **1. Tentukan luas jajaran genjang yang ditentukan oleh vektor $\vec{u} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad \vec{v} = \begin{bmatrix} 2 \\ 1 \end{bmatrix}$**

Dengan menambahkan komponen $z=0$ agar bisa menggunakan cross product:

$$
\vec{u} = \begin{bmatrix} 1 \\ 2 \\ 0 \end{bmatrix}, \quad \vec{v} = \begin{bmatrix} 2 \\ 1 \\ 0 \end{bmatrix}
$$

Hitung cross product:

$$
\vec{u} \times \vec{v} = \begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
1 & 2 & 0 \\
2 & 1 & 0
\end{vmatrix} = \vec{k}(-3)
$$

Luas jajaran genjang:

$$
A = \|\vec{u} \times \vec{v}\| = |{-3}| = 3
$$

<iframe src="https://www.geogebra.org/classic/zbqstsaj" width="800" height="600" style="border:0;"></iframe>

---

##### **2. Tentukan luas jajaran genjang yang ditentukan oleh vektor $\vec{u} = \begin{bmatrix} 2 \\ 0 \end{bmatrix}, \quad \vec{v} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}$**

Dengan menambahkan komponen $z=0$ agar bisa menggunakan cross product:

$$
\vec{u} = \begin{bmatrix} 2 \\ 0 \\ 0 \end{bmatrix}, \quad
\vec{v} = \begin{bmatrix} 0 \\ 3 \\ 0 \end{bmatrix}
$$

Hitunglah $\vec{u} \times \vec{v}$ menggunakan determinan:

$$
\vec{u} \times \vec{v} =
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
2 & 0 & 0 \\
0 & 3 & 0
\end{vmatrix}
= \vec{i}(0\cdot0 - 0\cdot3) - \vec{j}(2\cdot0 - 0\cdot0) + \vec{k}(2\cdot3 - 0\cdot0)
$$

$$
= \vec{i}(0) - \vec{j}(0) + \vec{k}(6) = 6\vec{k}
$$

Maka hasil dari $\vec{u} \times \vec{v}$ adalah:

$$
\vec{u} \times \vec{v} = \begin{bmatrix} 0 \\ 0 \\ 6 \end{bmatrix}
$$

Luas jajaran genjang adalah panjang dari vektor hasil cross product:

$$
\left\| \vec{u} \times \vec{v} \right\| = \sqrt{0^2 + 0^2 + 6^2} = \sqrt{36} = 6
$$

<iframe src="https://www.geogebra.org/classic/f7zhfxwa" width="800" height="600" style="border:0;"></iframe>

---

##### **3. Tentukan luas segitiga dengan titik-titik sudut $A = (0, 0, 0), \quad B = (1, 3, -1), \quad C = (2, 1, 1)$**

Hitung vektor:

$$
\vec{u} = \vec{AB} = (1, 3, -1) - (0, 0, 0) = (1, 3, -1)
$$
$$
\vec{v} = \vec{AC} = (2, 1, 1) - (0, 0, 0) = (2, 1, 1)
$$

Hitung cross product:

$$
\vec{u} \times \vec{v} = 
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
1 & 3 & -1 \\
2 & 1 & 1
\end{vmatrix}
= \vec{i}(3 \cdot 1 - (-1) \cdot 1) - \vec{j}(1 \cdot 1 - (-1) \cdot 2) + \vec{k}(1 \cdot 1 - 3 \cdot 2)
$$

$$
= \vec{i}(3 + 1) - \vec{j}(1 + 2) + \vec{k}(1 - 6)
= 4\vec{i} - 3\vec{j} - 5\vec{k}
$$

Panjang vektor hasil cross product:

$$
\left\| \vec{u} \times \vec{v} \right\| = \sqrt{4^2 + (-3)^2 + (-5)^2} = \sqrt{16 + 9 + 25} = \sqrt{50}
$$

Luas segitiga adalah:

$$
\text{Luas} = \frac{1}{2} \left\| \vec{u} \times \vec{v} \right\| = \frac{1}{2} \cdot \sqrt{50} = \frac{\sqrt{50}}{2} = \frac{5\sqrt{2}}{2}
$$

<iframe src="https://www.geogebra.org/classic/khbeqa9h" width="800" height="600" style="border:0;"></iframe>

---

##### **4. Tentukan luas segitiga dengan titik-titik sudut $A = (5, 2, -1), \quad B = (3, 6, 2), \quad C = (1, 0, 4)$**

Hitung vektor:

$$
\vec{u} = \vec{QP} = Q - P = (3,6,2) - (5,2,-1) = (-2, 4, 3)
$$

$$
\vec{v} = \vec{RP} = R - P = (1,0,4) - (5,2,-1) = (-4, -2, 5)
$$

Hitung cross product:

$$
\vec{u} \times \vec{v} =
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k} \\
-2 & 4 & 3 \\
-4 & -2 & 5
\end{vmatrix}
= \vec{i}(4 \cdot 5 - 3 \cdot (-2)) - \vec{j}(-2 \cdot 5 - 3 \cdot (-4)) + \vec{k}(-2 \cdot (-2) - 4 \cdot (-4))
$$

$$
= \vec{i}(20 + 6) - \vec{j}(-10 + 12) + \vec{k}(4 + 16)
= \vec{i}(26) - \vec{j}(2) + \vec{k}(20)
$$

$$
\vec{u} \times \vec{v} = (26, -2, 20)
$$

Hitung panjang vektor hasil cross product:

$$
\left\| \vec{u} \times \vec{v} \right\| = \sqrt{26^2 + (-2)^2 + 20^2} = \sqrt{676 + 4 + 400} = \sqrt{1080}
$$

$$
\frac{2}{1} \cdot \frac{1}{1080} = \frac{2}{1080}
$$

$$
\sqrt{1080} = \sqrt{36 \times 30} = 6\sqrt{30} \Rightarrow \text{Luas} = \frac{6\sqrt{30}}{2} = 3\sqrt{30}
$$

<iframe src="https://www.geogebra.org/classic/pqpcsjmm" width="800" height="600" style="border:0;"></iframe>

