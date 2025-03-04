---

Untuk menyelesaikan sistem persamaan linear menggunakan metode eliminasi Gauss, kita perlu memiliki tiga persamaan dengan tiga variabel. Mari kita buat tiga persamaan sebagai contoh:

$$
\begin{aligned}
  x + 2y + z = 4\\  
  2x + y - z = 1 \\ 
  3x - y + 2z = 7 
\end{aligned}
$$

Kita akan menyusun sistem persamaan ini dalam bentuk matriks augmented dan kemudian menggunakan metode eliminasi Gauss untuk menemukan solusi.

### Langkah 1: Menyusun Matriks Augmented

Matriks augmented untuk sistem di atas adalah:

$$
\begin{bmatrix}
1 & 2 & 1 & | & 4 \\
2 & 1 & -1 & | & 1 \\
3 & -1 & 2 & | & 7
\end{bmatrix}
$$

### Langkah 2: Eliminasi Gauss

Kita akan melakukan operasi baris elementer untuk mengubah matriks ini menjadi bentuk segitiga atas.

1. **Baris 2**: Kurangi 2 kali Baris 1 dari Baris 2
2. **Baris 3**: Kurangi 3 kali Baris 1 dari Baris 3

Setelah langkah pertama, matriks menjadi:

$$
\begin{bmatrix}
1 & 2 & 1 & | & 4 \\
0 & -3 & -3 & | & -7 \\
0 & -7 & -1 & | & -5
\end{bmatrix}
$$

3. **Baris 3**: Kurangi $$\frac{7}{3}$$ kali Baris 2 dari Baris 3

Setelah langkah kedua, matriks menjadi:

$$
\begin{bmatrix}
1 & 2 & 1 & | & 4 \\
0 & -3 & -3 & | & -7 \\
0 & 0 & 6 & | & 10
\end{bmatrix}
$$

### Langkah 3: Substitusi Balik

Sekarang kita akan menyelesaikan sistem persamaan dari bentuk segitiga atas ini.

Dari Baris 3:

$$
6z = 10 \implies z = \frac{10}{6} = \frac{5}{3}
$$

Dari Baris 2:
$$
-3y - 3z = -7 \implies -3y - 3\left(\frac{5}{3}\right) = -7 \implies -3y - 5 = -7 \implies -3y = -2 \implies y = \frac{2}{3}
$$

Dari Baris 1:
$$
x + 2y + z = 4 \implies x + 2\left(\frac{2}{3}\right) + \frac{5}{3} = 4
$$
$$
x + \frac{4}{3} + \frac{5}{3} = 4 \implies x + 3 = 4 \implies x = 1
$$

### Solusi Akhir

Jadi, solusi dari sistem persamaan ini adalah:
$$
x = 1, \quad y = \frac{2}{3}, \quad z = \frac{5}{3}
$$

Dengan demikian, garis yang berpotongan dengan ketiga persamaan tersebut adalah titik 
$$
(1, \frac{2}{3}, \frac{5}{3}) 
$$