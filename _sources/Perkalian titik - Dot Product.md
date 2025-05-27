---
title: Perkalian titik - Dot Product

---

### **Perkalian titik (Dot Product)**

#### **Pengertian Dot Product atau Perkalian Titik**
**Perkalian titik** atau **dot product** adalah sebuah operasi aljabar yang dilakukan pada dua vektor yang menghasilkan bilangan skalar (bukan vektor). Didefinisikan pada bilangan saklar : 

$$
\mathbf{v} \cdot \mathbf{w} = 
\begin{bmatrix}
v_1 \\
v_2
\end{bmatrix}
\cdot
\begin{bmatrix}
w_1 \\
w_2
\end{bmatrix}
= v_1w_1 + v_2w_2.
$$

---

#### **Operasi Dasar Vektor**
##### **Contoh 1**

**Misalnya:** 

$$
u = \begin{bmatrix} 3 \\ 0 \end{bmatrix}, \quad
a = \begin{bmatrix} 2 \\ 4 \end{bmatrix}, \quad
v = \begin{bmatrix} 3 \\ 4 \end{bmatrix}, \quad
w = \begin{bmatrix} 0 \\ 4 \end{bmatrix}
$$

**Hitung sudut antara $u$ dan $a$:**

* **Hitung Dot Product**

$$
u \cdot a = (3)(2) + (0)(4) = 6
$$

* **Hitung Panjang Vektor**

$$
|u| = \sqrt{3^2 + 0^2} = \sqrt{9} = 3
$$

$$
|a| = \sqrt{2^2 + 4^2} = \sqrt{4 + 16} = \sqrt{20} =\sqrt 4.472
$$

* **Mencari Sudut**

$$
\cos(\theta) = \frac{u \cdot a}{|u| \cdot |a|} = \frac{6}{3 \times \sqrt{20}} = \frac{6}{3 \times 4.472} = \frac{6}{13.416} =\sqrt 0.447
$$

$$
\theta = \cos^{-1}(0.447) =\sqrt 63.43^\circ
$$


<iframe src="https://www.geogebra.org/classic/rk5nae8h" width="800" height="600" style="border:0;"></iframe>

Karena $u \cdot a = 6 \neq 0$ maka, vektor $u$ dan $v$ **tidak ortogonal** (tidak tegak lurus), karena dot product-nya bukan nol.


##### **Contoh 2**

**Misalnya:**

$$u = \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \quad
v = \begin{bmatrix} -1 \\ 2 \end{bmatrix} \quad$$

**Hitung sudut antara $u$ dan $v$:**

* Hitung Dot Product

$$u \cdot v = (2)(-1) + (1)(2) = -2 + 2 = 0$$

* **Hitung Panjang Vektor**

$$
\|u\| = \sqrt{2^2 + 1^2} = \sqrt{4 + 1} = \sqrt{5}
$$

$$
\|v\| = \sqrt{(-1)^2 + 2^2} = \sqrt{1 + 4} = \sqrt{5}
$$

* **Mencari Sudut**

$$
0 = \sqrt{5} \cdot \sqrt{5} \cdot \cos\theta \implies 0 = 5 \cdot \cos\theta \implies \cos\theta = 0
$$

$$
\theta = \cos^{-1}(0) = 90^\circ
$$

<iframe src="https://www.geogebra.org/classic/te7hd5yr" width="800" height="600" style="border:0;"></iframe>

Karena $u \cdot v$ maka, vektor $u$ dan $v$ **Ortogonal** atau saling tegak lurus.

##### **Contoh 3**

**Misalnya:**

$$u = \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \quad
v = \begin{bmatrix} -2 \\ 4 \end{bmatrix} \quad$$

* **Hitung Dot Product**

$$
u \cdot v = (2)(-2) + (1)(4) = -4 + 4 = 0
$$

* **Hitung Panjang Vektor**

$$
\|u\| = \sqrt{2^2 + 1^2} = \sqrt{4 + 1} = \sqrt{5}
$$

$$
\|v\| = \sqrt{(-2)^2 + 4^2} = \sqrt{4 + 16} = \sqrt{20}
$$

* **Mencari Sudut**

$$
u \cdot v = \|u\| \|v\| \cos \theta \implies 0 = \|u\| \|v\| \cos \theta
$$

$$
\cos\theta = 0 \Rightarrow \theta = 90^\circ
$$

<iframe src="https://www.geogebra.org/classic/apqku3wz" width="800" height="600" style="border:0;"></iframe>

Karena $u \cdot v$ maka, vektor $u$ dan $v$ **Ortogonal** atau saling tegak lurus.



