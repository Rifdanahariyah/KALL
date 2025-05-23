## **Eigenvectors Eigenvalues**
#### **Definisi Eigenvectors dan Eigenvalues**

$$Av=λv$$ 

* Eigenvalues: skalar λ yang menyatakan seberapa besar vektor eigen mengalami peregangan atau pengecilan setelah dikalikan dengan matriks  A .

* Eigenvector: vektor yang tidak nol yang ketika menerima transformasi oleh suatu matriks, arahnya tetap, hanya panjang atau skalanya yang berubah. Artinya, setelah dikalikan dengan matriks, hasilnya tetap searah dengan vektor semula.

#### **Mencari Eigenvalues dan Eigenvectors**

```python
import numpy as np

A = np.array([[2, 1],
              [1, 2]])

eigenvalues, eigenvectors = np.linalg.eig(A)
print("Nilai eigen:")
print(eigenvalues)

print("\nVektor eigen:")
print(eigenvectors)

# Matriks kedua
A = np.array([[8, -10],
              [5, -7]])

eigenvalues, eigenvectors = np.linalg.eig(A)
print("\nNilai eigen:")
print(eigenvalues)

print("\nVektor eigen:")
print(eigenvectors)
```

```
Nilai eigen:
[3. 1.]

Vektor eigen:
[[ 0.70710678 -0.70710678]
 [ 0.70710678  0.70710678]]

Nilai eigen:
[ 3. -2.]

Vektor eigen:
[[0.89442719 0.70710678]
 [0.4472136  0.70710678]]
```

### **Definisi Eigenvector Ortonormal dan Ortogonal**

* Ortonormal: setiap vektor yang memiliki panjangnya = 1 (normal = 1.

* Ortogonal: terdiri dari dua vektor yang dianggap ortogonal adalaha ketika sudutnya saling tegak lurus.

#### **Contoh Ortonormal dan Ortogonal**

Menggunakan matriks:
$$
A = \begin{bmatrix}
5 & 2 \\
2 & 5
\end{bmatrix}
$$

* Mencari Eigenvalue
$$
\det(A - \lambda I) = 0 \implies
\det \begin{bmatrix}
5 - \lambda & 2 \\
2 & 5 - \lambda
\end{bmatrix} = 0
$$

$$
(5 - \lambda)^2 - 4 = 0
\Rightarrow \lambda^2 - 10 \lambda + 21 = 0
\Rightarrow (\lambda - 7)(\lambda - 3) = 0
$$

* Diketahui Eigenvalue:
$$
\lambda_1 = 7, \quad \lambda_2 = 3
$$

* Mencari Eigenvector:

Untuk $\lambda_1 = 7:$

$$
(A - 7I) \mathbf{v} = 0 \implies
\begin{bmatrix}
5 - 7 & 2 \\
2 & 5 - 7
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix} =
\begin{bmatrix}
-2 & 2 \\
2 & -2
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix} = 0
$$

$$
-2x + 2y = 0 \implies y = x
$$

Ambil $x = 1$, maka:
$$
\mathbf{v}_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

Untuk $\lambda_2 = 3:$

$$
(A - 3I) \mathbf{v} = 0 \implies
\begin{bmatrix}
5 - 3 & 2 \\
2 & 5 - 3
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix} =
\begin{bmatrix}
2 & 2 \\
2 & 2
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix} = 0
$$

$$
2x + 2y = 0 \implies y = -x
$$

Ambil $x = 1$, maka:

$$
\mathbf{v}_2 = \begin{bmatrix} 1 \\ -1 \end{bmatrix}
$$

* Ortogonal
$$
\mathbf{v}_1 \cdot \mathbf{v}_2 = (1)(1) + (1)(-1) = 1 - 1 = 0
$$

* Ortonormal
$$
\|\mathbf{v}_1\| = \sqrt{1^2 + 1^2} = \sqrt{2} \implies
\mathbf{u}_1 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

$$
\|\mathbf{v}_2\| = \sqrt{1^2 + (-1)^2} = \sqrt{2} \implies
\mathbf{u}_2 = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\ -1 \end{bmatrix}
$$


