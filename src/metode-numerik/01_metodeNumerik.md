# Pengantar Metode Numerik

## Apa itu Metode Numerik?
- Numerik: berhubungan dengan angka
- Metode: cara yang sistematis untuk menyelesaikan persoalan guna mencapai tujuan yang ditentukan
<br>
- Metode numerik: cara sistematis untuk menyelesaikan persoalan matematika dengan operasi angka (+, -, \*, /)
<br>
Contoh beberapa persoalan matematika:
1. Tentukan akar-akar persamaan polinom
	### $23.4x^7-1.25x^6+120x^4+15x^3-120x^2-x+100=0$
2. Tentukan x yang memenuhi persamaan:
	### $\sqrt{17.8e^{5x}-\frac{1}{x}}=\cos^{-1}\frac{(120x^2+\sqrt{2x})}{17x-65}$
3. Hitung nilai integral-tentu berikut:
	### $\int_{1.2}^{2.5}(\sqrt{(45.3e^{7x}+\frac{100}{x})^4}+\frac{4}{x^2+1})$
4. Diberikan persamaan differensial biasa (PDB) dengan sebuah niali awal:
\*belum selesai.....

- Cara penyelesaian persoalan matematika ada dua:
	1. Secara analitik
	2. Secara numerik

- Secara analitik: menggunakan rumus dan teorama yang sudah baku dalam matematika -> metode analitik.

Contoh: $x^2-6x+8=0$ -> carilah akar-akarnya!
Metode analitik: faktorkan menjadi $(x-4)(x-2)=0$
> $x-4=0 -> x_1 = 4$
> $x-2=0 -> x_2 = 2$

- Secara numerik: menggunakan pendekatan aproksimasi untuk mencari solusi hanya dengan operasi aritmatika biasa -> metode numerik.

Contoh: carilah sebuah akar $f(x)=x^2-6x+8=0$
Metode numerik: diketahui sebuah akar terletak di dalam selang [3, 6] -> mengapa?
![gambar1.1](mn1.1.png)
Pendekatan sederhana mencari akar adalah secara iteratif dengan **metode titik tengah** (bisection):
1. bagi selang[a,b] menjadi dua dengan titik tengah $c=(a+b)/2$
2. ada dua sub-selang: [a,c] dan [c,b]. Pilih selang iterasi yang baru dengan syarat nilai fungsi di ujung selang berbeda tanda.
3. ulangi langkah 1 dan 2 sampai ukuran selang $<\epsilon$ (epsilon adalah nilai yang sangat kecil yang menyatakan toleransi kesalahan akar yang diinginkan, misalnya $\epsilon=0.001, 00001, dsb$)
![gambar1.2 height=500px](/assets/img/metode-numerik/mn1.2.png)

\*belum selesai :|