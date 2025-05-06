## **Transformasi linier dan Refleksi**

### **Transformasi Linier**
Transformasi linier adalah suatu fungsi atau pemetaan dari ruang vektor ke ruang vektor lain (atau ke dirinya sendiri), yang memenuhi dua sifat utama, yaitu:

#### **Sifat Additivitas (Penjumlahan Vektor)**
Pembuktian bahwa transformasi

$$
T(v_1, v_2) = (v_1 - v_2, v_1 + 2v_2)
$$

memenuhi **sifat aditif** dari transformasi linier, yaitu:

$$
T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})
$$ 
<br>


##### Langkah 1: Misalkan dua vektor di $\mathbb{R}^2$

* $\mathbf{u} = (u_1, u_2)$
* $\mathbf{v} = (v_1, v_2)$
<br>

##### Langkah 2: Hitung $\mathbf{u} + \mathbf{v}$

$$
\mathbf{u} + \mathbf{v} = (u_1 + v_1, u_2 + v_2)
$$
<br>

##### Langkah 3: Hitung $T(\mathbf{u} + \mathbf{v})$

Karena $T(x, y) = (x - y, x + 2y)$, maka:

$$
T(\mathbf{u} + \mathbf{v}) = T(u_1 + v_1,\ u_2 + v_2)
$$

$$
= ((u_1 + v_1) - (u_2 + v_2),\ (u_1 + v_1) + 2(u_2 + v_2))
$$

$$
= (u_1 - u_2 + v_1 - v_2,\ u_1 + 2u_2 + v_1 + 2v_2)
$$
<br>


##### Langkah 4: Hitung $T(\mathbf{u}) + T(\mathbf{v})$

$$
T(\mathbf{u}) = (u_1 - u_2,\ u_1 + 2u_2)
$$

$$
T(\mathbf{v}) = (v_1 - v_2,\ v_1 + 2v_2)
$$

$$
T(\mathbf{u}) + T(\mathbf{v}) = (u_1 - u_2 + v_1 - v_2,\ u_1 + 2u_2 + v_1 + 2v_2)
$$
<br>


##### Langkah 5: Bandingkan hasilnya

Kita dapat melihat bahwa:

$$
T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})
$$

Jadi **sifat additivitas (penjumlahan vektor)** terbukti berlaku sebagai Trasformasi Linier.

<br> 

#### **Sifat Homogenitas (Perkalian Skalar)**

Mari kita bahas secara **jelas dan lengkap** tentang **sifat homogenitas (perkalian skalar)** untuk membuktikan bahwa suatu fungsi $T: \mathbb{R}^2 \rightarrow \mathbb{R}^2$ adalah **transformasi linier**.


Sifat homogenitas menyatakan bahwa untuk setiap **skalar $c \in \mathbb{R}$** dan **vektor $\mathbf{v} \in \mathbb{R}^2$** berlaku:

$$
T(c\mathbf{v}) = c \cdot T(\mathbf{v})
$$


##### **Contoh Uji Homogenitas pada Transformasi**

Misalkan transformasi:

$$
T(v_1, v_2) = (v_1 - v_2,\ v_1 + 2v_2)
$$

Uji apakah fungsi ini memenuhi sifat homogenitas.



##### 1. **Misalkan sebuah vektor**

$$
\mathbf{v} = (v_1, v_2)
$$

##### 2. **Kalikan vektor dengan skalar $c$**

$$
c \cdot \mathbf{v} = (cv_1, cv_2)
$$



##### 3. **Hitung $T(c \cdot \mathbf{v})$**

$$
T(cv_1, cv_2) = (cv_1 - cv_2,\ cv_1 + 2cv_2)
= c(v_1 - v_2,\ v_1 + 2v_2)
$$


##### 4. **Hitung $c \cdot T(\mathbf{v})$**

$$
T(v_1, v_2) = (v_1 - v_2,\ v_1 + 2v_2)
\Rightarrow c \cdot T(\mathbf{v}) = c(v_1 - v_2,\ v_1 + 2v_2)
$$


##### Bandingkan hasilnya:

$$
T(c\mathbf{v}) = c \cdot T(\mathbf{v})
$$

Jadi, **sifat homogenitas terpenuhi.**



#####  **Kesimpulan:**

Jika kita sudah menunjukkan bahwa:

* $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$ (**aditivitas**)
* $T(c\mathbf{v}) = cT(\mathbf{v})$ (**homogenitas**)

Maka **$T$ adalah transformasi linier.**



---

Berikut **2 contoh titik berbeda** untuk masing-masing jenis refleksi **beserta hasil refleksinya**:



#### 1. Refleksi terhadap sumbu-x

$$
\begin{bmatrix}
1 & 0 \\
0 & -1 \\
\end{bmatrix}
$$

* A(4, 5) → **A′(4, -5)**

<iframe src="https://www.geogebra.org/classic/tkerxa7p"
width="800" height="600" style="border:0;"></iframe>


#### 2. Refleksi terhadap sumbu-y

$$
\begin{bmatrix}
-1 & 0 \\
0 & 1 \\
\end{bmatrix}
$$

* B(2, 6) → **B′(-2, 6)**

<iframe src="https://www.geogebra.org/classic/hffaydct"
width="800" height="600" style="border:0;"></iframe>


#### 3. Refleksi terhadap garis y = x

$$
\begin{bmatrix}
0 & 1 \\
1 & 0 \\
\end{bmatrix}
$$

* C(8, 1) → **C′(1, 8)**

<iframe src="https://www.geogebra.org/classic/nsnyhzhc"
width="800" height="600" style="border:0;"></iframe>



#### 4. Refleksi terhadap garis y = -x

$$
\begin{bmatrix}
0 & -1 \\
-1 & 0 \\
\end{bmatrix}
$$

* D(5, -2) → **D′(2, -5)**

<iframe src="https://www.geogebra.org/classic/p4akjnch"
width="800" height="600" style="border:0;"></iframe>


#### 5. Refleksi terhadap titik asal

$$
\begin{bmatrix}
-1 & 0 \\
0 & -1 \\
\end{bmatrix}
$$

* E(6, 8) → **E′(6,-8)**

<iframe src="https://www.geogebra.org/classic/zujaa6rm"
width="800" height="600" style="border:0;"></iframe>

---




### **Refleksi Y = X**

import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

##### Titik-titik objek asli (misalnya, segitiga 3D)
points = np.array([
    [1, 5, 1],
    [2, 2, 1],
    [3, 2, 1]
]).T  # bentuknya 3xN

##### Matriks refleksi terhadap garis y = x (dalam ruang 3D)
reflection_matrix = np.array([
    [0, 1, 0],
    [1, 0, 0],
    [0, 0, 1]
])

##### Lakukan refleksi
reflected_points = reflection_matrix @ points

##### Buat plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

##### Gambar objek asli (biru)
ax.plot(points[0], points[1], points[2], 'bo-', label='Asli')

##### Gambar objek setelah refleksi (merah)
ax.plot(reflected_points[0], reflected_points[1], reflected_points[2], 'ro-', label='Refleksi')

##### Set aspek dan label
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')
ax.set_title('Refleksi terhadap garis y = x')
ax.legend()
ax.set_box_aspect([1,1,1])  # aspek rasio 1:1:1

plt.show()
