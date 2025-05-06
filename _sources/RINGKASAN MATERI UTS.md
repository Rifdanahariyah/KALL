## RINGKASAN DAN TUGAS (Transformasi Matriks) 

* ##### **Transformasi Matriks**
Transformasi Matriks yaitu bagaimana matriks dapat digunakan untuk mengubah satu vektor menjadi vektor lainnya. 
Dengan menggunakan matriks $A$ berukuran $m$ X $n$ bisa digunakan untuk mendefinisikan sebuah fungsi $T$ yang mengambil vektor kolom $\vec{x}$ adalah vektor kolom berukuran $n \times 1$ dan menghasilkan vektor kolom $\vec{y}$ berukuran $m \times 1$ melalui persamaan:

$$
\vec{y} = T(\vec{x}) = A\vec{x}
$$

Fungsi ini disebut **Transformasi Matriks**, dan termasuk dalam kelas umum yang biasanya disebut **Transformasi Linier** yaitu fungsi antar vektor

---

* ##### **Perkalian Matriks - Vektor**

Agar hasil perkalian tetap berupa vektor  2D $(\ \mathbb{R}^2)$, maka matriks $A$ harus berukuran $2$ X $2$. 
Diberikan matriks $A$ dan tiga vektor $\vec{x},\ \vec{y},\ \vec{z}$ hasil perkalian antara matriks dan vektor dihitung sebagai berikut:

$$
A = \begin{bmatrix}
4 & 2 \\
1 & 3
\end{bmatrix}, \quad
\vec{x} = \begin{bmatrix}
1 \\
1
\end{bmatrix}, \quad
\vec{y} = \begin{bmatrix}
-1 \\
1
\end{bmatrix}, \quad
\vec{z} = \begin{bmatrix}
3 \\
-1
\end{bmatrix}
$$

Solusi:

$$
A\vec{x} = \begin{bmatrix}
5 \\
5
\end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix}
-3 \\
1
\end{bmatrix}, \quad
A\vec{z} = \begin{bmatrix}
-1 \\
3
\end{bmatrix}
$$

Perkalian matriks mengubah panjang dan arah vektor dalam contoh di atas vektor $\vec{x}$ dan $A\vec{x}$ memiliki arah yang sama tapi panjangnya yang berubah. Namun, $\vec{y}$ dan $\vec{z}$ beruubah arah saat dikalikan dengan $A$. Hal ini menunjukkan bahwa matriks bertindak secara berbeda terhadap vektor yang berbeda.

---

* ##### **Menggabungkan penjumlahan dan perkalian matriks**

Diketahui:

$$
A = \begin{bmatrix}
1 & 1 \\
1 & 2
\end{bmatrix}, \quad
\vec{x} = \begin{bmatrix}
2 \\
1
\end{bmatrix}, \quad
\vec{y} = \begin{bmatrix}
-1 \\
1
\end{bmatrix}
$$

Sketsa: $\vec{x} + \vec{y}$,$A\vec{x}$,$A\vec{y}$ dan $A(\vec{x}+\vec{y})$

langkah ini bertujuan untuk melihat bagaimana penjumlahan vektor berinteraksi dengan transformasi matriks.

Dihitung:

$$
\vec{x} + \vec{y} = \begin{bmatrix}
1 \\
2
\end{bmatrix}, \quad
A\vec{x} = \begin{bmatrix}
3 \\
4
\end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix}
0 \\
1
\end{bmatrix}, \quad
A(\vec{x} + \vec{y}) = \begin{bmatrix}
3 \\
5
\end{bmatrix}
$$

Ini menunjukkan **sifat distributif** dari perkalian matriks terhadap penjumlahan vektor: $$A(\vec{x} + \vec{y}) = A\vec{x} + A\vec{y}$$

---

* ##### **Menggambar Efek dari Perkalian matriks**

Diketahui:

$$
A = \begin{bmatrix}
1 & 1 \\
-1 & -1
\end{bmatrix}, \quad
\vec{x} = \begin{bmatrix}
1 \\
1
\end{bmatrix}, \quad
\vec{y} = \begin{bmatrix}
-1 \\
1
\end{bmatrix}, \quad
\vec{z} = \begin{bmatrix}
4 \\
4
\end{bmatrix}
$$

Solusi:

$$
A\vec{x} = \begin{bmatrix}
0 \\
0
\end{bmatrix} \quad 
A\vec{y} = \begin{bmatrix}
-2 \\
-2
\end{bmatrix} \quad
and \quad
A\vec{z} = \begin{bmatrix}
3 \\
3\end{bmatrix}
$$

Beberapa vektor seperti $(\vec{x}$ dan $\vec{y})$ setelah dikalikan dengan matriks, hasilnya adalah vektor nol sementara vektor lain tetepa berada pada garis tertentu.

---

* ##### **Transformasi terhadap bidang kartesius**

Pada bagian ini memeperkenalkan transisi dan menggambarkan vektor satu per satu ke menggambarkan bagaimana seluruh bidang katresius $(\mathbb{R}^2)$berubah oleh matriks.

___

* ##### **Visualisasi Transformasi Matriks Menggunnakan vektor**

efek transformasi terhadap seluruh bidang Kartesius dengan melihat bagaimana **persegi satuan (unit square)** berubah.
Misalkan: 

$$
A = \begin{bmatrix}
1 & 4 \\
2 & 3
\end{bmatrix}
$$

Titik - titik sudut dari persegi satuan berada di:

$$
\begin{bmatrix}
0 \\
0
\end{bmatrix}, \quad
\begin{bmatrix}
1 \\
0
\end{bmatrix}, \quad
\begin{bmatrix}
1 \\
1
\end{bmatrix}, \quad
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

Setelah dikalikan deng $A$, titik - titik tersebut menjadi:

$$
\begin{bmatrix}
0 \\
0
\end{bmatrix}, \quad
\begin{bmatrix}
1 \\
2
\end{bmatrix}, \quad
\begin{bmatrix}
5 \\
5
\end{bmatrix}, \quad
\begin{bmatrix}
4 \\
3
\end{bmatrix}
$$

Adapun tips cepat untuk menggunakan matriks kolom: 
Buat matriks $B$ yang kolom - kolomnya adalah titik - titik susdut:

$$
B = \begin{bmatrix}
0 & 1 & 1 & 0 \\
0 & 0 & 1 & 1
\end{bmatrix}
$$

Dikalikan:

$$
AB = \begin{bmatrix}
0 & 2 & 6 & 4 \\
0 & 1 & 4 & 3
\end{bmatrix}
$$

Proses ini cepat jika harus dilakukan transformasi pada banyak titik sekaligus

Perubahan bentuk dari persegi satuan setelah dikalikan dengan matriks:

$$
A = \begin{bmatrix}
1 & 4 \\
2 & 3
\end{bmatrix}
$$ 

Menghasilkan persegi berubah menjadi jajargenjang. Selain merenggang, bentuknya juga tampak terbalik, seolah titik - titik segitiga dan persegi saling bertukar tempat.

![Cuplikan layar 2025-04-13 200922](https://hackmd.io/_uploads/rJGzYNYR1x.png)

menggambarkan bahwa garis-garis lurus pada persegi satuan tetap lurus setelah transformasi oleh matriks, meskipun bentuknya berubah.

* ##### **Transformasi Matriks terhadap sebuah wilayah**

Matriks yang digunakan: 

$$
A = \begin{bmatrix}
0 & -1 \\
1 & 0
\end{bmatrix}
$$ 

Matriks ini merupakan rotasi 90 derajat berlawanan arah jarum jam terhadap titik asal (0,0) dalam bidang kartesius.
Contoh diberikan dengan menggunakan matriks:

$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$ 

hasil perkalian: 

$$
A\vec{e_1} = \begin{bmatrix}
a \\ c
\end{bmatrix} \quad
A\vec{e_2} = \begin{bmatrix}
a \\ c
\end{bmatrix}
$$ 

dapat dilihat bahwa kolom pertama dan kedua dari $𝐴$ menentukan ke mana titik (1,0) dan (0,1) berpindah, yang berarti kita bisa menyusun kembali matriks transformasi jika kita tahu ke mana kedua titik ini dipetakan.

---

* ##### **Macam - macam Transformasi umum**
Beberapa transformasi umum dan matriksnya:

* Vertical Stretch:

$
\begin{bmatrix}1 & 0 \\0 & k\end{bmatrix}
$

* Horizontal Shear:

$
\begin{bmatrix}1 & k \\0 & 1\end{bmatrix}
$

* Vertical Shear:

$
\begin{bmatrix}1 & 0 \\k & 1\end{bmatrix}
$

* Horizontal Reflection (sumbu $y$):

$
\begin{bmatrix}-1 & 0 \\0 & 1\end{bmatrix}
$

* Vertical Reflection (sumbu $x$):

$
\begin{bmatrix}1 & 0 \\0 & -1\end{bmatrix}
$

* Refleksi Diagonal ($y = x$):

$
\begin{bmatrix}0 & 1 \\1 & 0\end{bmatrix}
$

* Rotasi sebesar sudut $\theta$:

$
\begin{bmatrix}\cos \theta & -\sin \theta \\\sin \theta & \cos \theta\end{bmatrix}
$

* Proyeksi ke sumbu $x$:

$
\begin{bmatrix}1 & 0 \\0 & 0\end{bmatrix}
$

---
### TUGAS

#### **SOAL 1**
Diketahui : 

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}, \quad 
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad 
\vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
$$

Penyelesaian:

**Hitung $A\vec{x}$**

Misalkan:

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}, \quad \vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

Perkalian matriks:

$$
A\vec{x} = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix}
= \begin{bmatrix} 1 \times 1 + (-1) \times 1 \\ 2 \times 1 + 3 \times 1 \end{bmatrix}
= \begin{bmatrix} 1 - 1 \\ 2 + 3 \end{bmatrix}
= \begin{bmatrix} 0 \\ 5 \end{bmatrix}
$$

Penyelesaian:

**Hitung $A\vec{y}$**

Misalkan:

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}, \quad \vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
$$

Perkalian matriks:

$$
A\vec{y} = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} -1 \\ 2 \end{bmatrix}
= \begin{bmatrix} 1 \times (-1) + (-1) \times 2 \\ 2 \times (-1) + 3 \times 2 \end{bmatrix}
= \begin{bmatrix} -1 - 2 \\ -2 + 6 \end{bmatrix}
= \begin{bmatrix} -3 \\ 4 \end{bmatrix}
$$

---

#### **SOAL 2**

Diketahui:

$$
A = \begin{bmatrix} 2 & -1 \\ 0 & 3 \end{bmatrix}, \quad
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
$$

Perkalian matriks:

**Hitung $A\vec{x}$**

$$
A\vec{x} = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
\begin{bmatrix} 1 \\ 1 \end{bmatrix}
= \begin{bmatrix} 2 \cdot 1 + 0 \cdot 1 \\ -1 \cdot 1 + 3 \cdot 1 \end{bmatrix}
= \begin{bmatrix} 2 \\ 2 \end{bmatrix}
$$

Perkalian matriks:

**Hitung $A\vec{y}$**

$$
A\vec{y} = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
\begin{bmatrix} -1 \\ 2 \end{bmatrix}
= \begin{bmatrix} 2 \cdot (-1) + 0 \cdot 2 \\ -1 \cdot (-1) + 3 \cdot 2 \end{bmatrix}
= \begin{bmatrix} -2 \\ 7 \end{bmatrix}
$$

---

#### **SOAL 5**

![Cuplikan layar 2025-04-11 105341](https://hackmd.io/_uploads/rJFPMzLRyx.png)

Dari gambar diketahui transformasi berikut:

$$
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \rightarrow \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix} \rightarrow \begin{bmatrix} 1 \\ 3 \end{bmatrix}
$$

Maka matriks transformasinya adalah:

$$
A = \begin{bmatrix} 1 & 1 \\ 2 & 3 \end{bmatrix}
$$

---

#### **SOAL 6**

![Cuplikan layar 2025-04-11 105349](https://hackmd.io/_uploads/SyG2VGL0ye.png)


Dari gambar diketahui transformasi berikut:

$$
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \rightarrow \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix} \rightarrow \begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

Maka matriks transformasinya adalah:

$$
A = \begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}
$$

-----

## **TRANSFORMASI LINIER**
### **Refleksi X = 2**

```python
import numpy as np
import matplotlib.pyplot as plt

# Titik-titik asal (koordinat domain)
x = np.array([-1, 0, 1])
y = np.array([1, 0, -1])

# Membuat matriks koordinat dalam bentuk 2xN
koordinats = np.vstack((x, y))

# Matriks transformasi refleksi terhadap sumbu Y
B = np.array([[-1, 0],
              [ 0, 1]])

# Transformasi bayangan (codomain)
B_trans = B @ koordinats
x_LT2 = B_trans[0, :]
y_LT2 = B_trans[1, :]

# Membuat gambar dan sumbu
fig, ax = plt.subplots()

# Plot titik asal (merah) dan bayangan (biru)
ax.plot(x, y, 'ro', label='Asal (Domain)')
ax.plot(x_LT2, y_LT2, 'bo', label='Bayangan (Codomain)')

# Garis penghubung titik
ax.plot(x, y, 'r--')
ax.plot(x_LT2, y_LT2, 'b-')

# Gambar sumbu X dan Y
ax.axvline(x=0, color='k', linestyle=':')
ax.axhline(y=0, color='k', linestyle=':')

# Tambahkan garis vertikal di x = 2
ax.axvline(x=2, color='g', linestyle='--', label='x = 2')

# Set pengaturan sumbu
ax.grid(True)
ax.axis([-2, 2.5, -1.5, 2])
ax.set_aspect('equal')
ax.set_title("Refleksi terhadap Sumbu X=2")
ax.legend()

# Tampilkan grafik
plt.show()
```

### **Refleksi Y = 2**

```python
import numpy as np
import matplotlib.pyplot as plt

# Titik-titik asal (domain)
x = np.array([-1, 0, 1])
y = np.array([1, 0, -1])

# Refleksi terhadap garis y = 2
y_LT2 = 4 - y  # karena 2*2 - y
x_LT2 = x      # x tidak berubah

# Membuat gambar dan sumbu
fig, ax = plt.subplots()

# Plot titik asal dan bayangan
ax.plot(x, y, 'ro', label='Asal (Domain)')
ax.plot(x_LT2, y_LT2, 'bo', label='Bayangan (Codomain)')

# Garis penghubung
ax.plot(x, y, 'r--')
ax.plot(x_LT2, y_LT2, 'b-')

# Gambar sumbu dan garis y = 2
ax.axvline(x=0, color='k', linestyle=':')
ax.axhline(y=0, color='k', linestyle=':')
ax.axhline(y=2, color='g', linestyle='--', label='y = 2')

# Atur tampilan
ax.grid(True)
ax.axis([-2, 2.5, -2, 5])
ax.set_aspect('equal')
ax.set_title("Refleksi terhadap Garis y = 2")
ax.legend()

# Tampilkan
plt.show()
```

### **Refleksi terhadap garis y = x**

```python
import numpy as np
import matplotlib.pyplot as plt

# Titik-titik asal (domain)
x = np.array([-1, 0, 1])
y = np.array([1, 0, -1])

# Membuat vektor koordinat 2xN
koordinats = np.vstack((x, y))

# Matriks refleksi terhadap garis y = x
B = np.array([[0, 1],
              [1, 0]])

# Transformasi bayangan (codomain)
B_trans = B @ koordinats
x_LT2 = B_trans[0, :]
y_LT2 = B_trans[1, :]

# Membuat gambar dan sumbu
fig, ax = plt.subplots()

# Plot titik asal dan bayangan
ax.plot(x, y, 'ro', label='Asal (Domain)')
ax.plot(x_LT2, y_LT2, 'bo', label='Bayangan (Codomain)')

# Garis penghubung
ax.plot(x, y, 'r--')
ax.plot(x_LT2, y_LT2, 'b-')

# Gambar sumbu dan garis y = x
ax.axvline(x=0, color='k', linestyle=':')
ax.axhline(y=0, color='k', linestyle=':')
x_line = np.linspace(-2, 2, 100)
ax.plot(x_line, x_line, 'g--', label='y = x')

# Atur tampilan
ax.grid(True)
ax.axis([-2, 2.5, -2, 2.5])
ax.set_aspect('equal')
ax.set_title("Refleksi terhadap Garis y = x")
ax.legend()

# Tampilkan
plt.show()
```
