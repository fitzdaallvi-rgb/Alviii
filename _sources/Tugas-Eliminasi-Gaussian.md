# Tugas Eliminasi Gaussian



## Persamaan Linier

Soal

Diberikan sistem persamaan linear dengan lima variabel berikut:


$$
\begin{cases}
0x_1 + 0x_2 + 2x_3 + 0x_4 + 3x_5 = 21 \\
2x_1 + 1x_2 + x_3 + 0x_4 + 0x_5 = 7 \\
0x_1 + 0x_2 + 1x_3 + 0x_4 + 0x_5 = 3 \\
2x_1 + 0x_2 + 4x_3 + x_4 + x_5 = 23 \\
1x_1 + 2x_2 + x_3 + 0x_4 + x_5 = 13
\end{cases}
$$


## Matriks Augmented

Sistem persamaan di atas dapat dituliskan dalam bentuk matriks augmented sebagai berikut:


$$
\left[
\begin{array}{ccccc|c}
0 & 0 & 6 & 0 & 15 & 21 \\
2 & 2 & 3 & 0 & 0 & 7 \\
0 & 0 & 3 & 0 & 0 & 3 \\
2 & 0 & 12 & 4 & 5 & 23 \\
1 & 4 & 3 & 0 & 5 & 13
\end{array}
\right]
$$


## Eliminasi Gaussian

### Langkah 1: Menentukan pivot pertama

Elemen pada baris pertama kolom pertama bernilai 0 sehingga tidak dapat dijadikan pivot. Oleh karena itu baris pertama ditukar dengan baris kedua.

Operasi baris: 

$$
R₁ ↔ R₂
$$

Matriks menjadi:


$$
\left[
\begin{array}{ccccc|c}
0 & 0 & 6 & 0 & 15 & 21 \\
2 & 2 & 3 & 0 & 0 & 7 \\
0 & 0 & 3 & 0 & 0 & 3 \\
2 & 0 & 12 & 4 & 5 & 23 \\
1 & 4 & 3 & 0 & 5 & 13
\end{array}
\right]
$$

Penjelasan:

1. Pivot pertama dicari pada kolom 1.

2. Baris pertama memiliki nilai 0, sehingga tidak bisa dijadikan pivot.

3. Baris kedua memiliki nilai 2, sehingga baris pertama dan baris kedua ditukar.


### Langkah 2: Nolkan elemen di bawah pivot kolom 1

Pivot berada pada kolom 1 baris 1 (angka 2).
Selanjutnya kita membuat elemen di bawahnya menjadi 0.

Operasi baris:

$$
R_4 \leftarrow R_4 - R_1
$$

$$
R_5 \leftarrow R_5 - \frac{1}{2}R_1
$$

Matriks menjadi:


$$
\left[
\begin{array}{ccccc|c}
0 & 0 & 6 & 0 & 15 & 21 \\
2 & 2 & 3 & 0 & 0 & 7 \\
0 & 0 & 3 & 0 & 0 & 3 \\
2 & 0 & 12 & 4 & 5 & 23 \\
1 & 4 & 3 & 0 & 5 & 13
\end{array}
\right]
$$

Penjelasan:

1. Pivot pertama berada pada kolom 1 baris 1 dengan nilai 2.

2. Pada baris 4 kolom 1 terdapat angka 2 sehingga harus dinolkan.

3. Nilai tersebut dinolkan dengan mengurangi baris 4 dengan baris 1.

4. Pada baris 5 kolom 1 terdapat angka 1, sehingga dinolkan dengan mengurangi setengah dari baris 1.


### Langkah 3: Menentukan pivot kolom 2

Karena elemen pada baris 2 kolom 2 = 0, maka kita menukar baris kedua dengan baris kelima.

Operasi baris:

$$
R_2 \leftrightarrow R_5
$$

Matriks menjadi:


$$
\left[
\begin{array}{ccccc|c}
2 & 2 & 3 & 0 & 0 & 7 \\
0 & 3 & 1.5 & 0 & 5 & 9.5 \\
0 & 0 & 3 & 0 & 0 & 3 \\
0 & -2 & 9 & 4 & 5 & 16 \\
0 & 0 & 6 & 0 & 15 & 21
\end{array}
\right]
$$

Penjelasan:
1. Pivot kedua harus berada pada kolom 2.

2. Elemen pada baris 2 kolom 2 bernilai 0, sehingga tidak bisa dijadikan pivot.

3. Pada baris 5 kolom 2 terdapat angka 3, sehingga baris kedua ditukar dengan baris kelima.


### Langkah 4: Nolkan elemen di bawah pivot kolom 2

Pivot kedua berada pada baris 2 kolom 2 (nilai 3).

Operasi baris:

$$
R_4 \leftarrow R_4 + \frac{2}{3}R_2
$$

Matriks menjadi:


$$
\left[
\begin{array}{ccccc|c}
2 & 2 & 3 & 0 & 0 & 7 \\
0 & 3 & 1.5 & 0 & 5 & 9.5 \\
0 & 0 & 3 & 0 & 0 & 3 \\
0 & 0 & 10 & 4 & \frac{25}{3} & \frac{67}{3} \\
0 & 0 & 6 & 0 & 15 & 21
\end{array}
\right]
$$

Penjelasan:
1. Pivot kedua berada pada baris 2 kolom 2.

2. Di bawah pivot terdapat angka -2 pada baris 4 kolom 2.

3. Untuk menolkan angka tersebut kita menambahkan 2/3 kali baris 2 ke baris 4.


### Langkah 5: Nolkan elemen di bawah pivot kolom 3

Pivot ketiga berada pada baris 3 kolom 3 (angka 3).

Operasi baris:

$$
\begin{aligned}
R_4 &\leftarrow R_4 - \frac{10}{3}R_3 \\
R_5 &\leftarrow R_5 - 2R_3
\end{aligned}
$$

Matriks menjadi:


$$
\begin{aligned}
R_4 &\leftarrow R_4 - \frac{10}{3}R_3 \\
R_5 &\leftarrow R_5 - 2R_3
\end{aligned}
$$

Penjelasan:
1. Pivot ketiga berada pada baris 3 kolom 3.

2. Di bawah pivot terdapat angka 10 pada baris 4 dan 6 pada baris 5.

3. Kedua elemen tersebut dinolkan dengan mengurangi kelipatan dari baris 3.


## Hasil Penyelesaian

Dari baris terakhir diperoleh:

$$
15x_5 = 15
$$

sehingga

$$
x_5 = 1
$$

Kemudian dilakukan substitusi ke atas sehingga diperoleh:

$$
x_4 = 1
$$

$$
x_3 = 1
$$

$$
x_2 = 1
$$

$$
x_1 = 1
$$


## Sage cell


![Sage Cell](grafik/sage_cell.png)
