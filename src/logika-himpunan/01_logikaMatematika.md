## Definisi Logika
- Logika (logic) berasal dari kata bahasa Yunani "logos"
- Definisi logika:
	- Ilmu tentang metode penalaran yang berhubungan dengan pembuktian validitas suatu argumen.
	- Suatu argumen yang brisi pernyataan harus diubah menjadi bentuk logika agar dapat dibuktikan validitasnya.
	- Pernyataan adalah kalimat yang memiliki arti dan dapat diberi nilai benar atau salah.
	- Contoh pernyataan:
		- Aku suka kamu
		- Aku suka dia
## Penalaran Deduktif dari Logika
- Logika berkaitan dengan penalaran deduktir (deductive reasoning) yang secara umum hanya mengambil kesimpulan (K) dari premis-premisnya (P).
- Berbeda dengan penalaran induktif (inductive reasoning), yaitu pegambilan kesimpulan umum yang diperoleh dari suatu observasi.
- Contoh:
	- Semua yang mengendarai sepeda memakai topi.
	- Joko mengendarai sepeda.
		## Dengan demikian, Joko memakai sepatu.

## Peranan Logika
- Bidang Matematika
	- Komputasi
	- Matematika Diskret
	- Aljabar Linier
- Elektronika
	- Rangkaian Digital
- Ilmu Komputer / Informatika
	- Membuat dan menguji program komputer
	- Artifical Intelligence
	- Expert Systems
	- Logic Programming
	- Soft Computing

## Argumen
- Argumen adalah usaha untuk mencari kebenaran dari suatu pernyataan berupa kesimpulan dengan berdasarkan kebenaran dari banyaknya pernyataan yang disebut dengan premis-premis.
- Argumen berbentuk sekumpulan pernyataan yang terdiri dari premis-premis dan diikuti satu kesimpulan.

- Contoh 1:
	- P1: Semua pelajar pandai.
	- P2: Ahmad adalah seorang pelajar
	- K: **Ahmad pandai**

- Contoh 2:
	- P1: Semua pelari pasti menggerakkan kakinya
	- P2: Dian sedang menggerakkan kakinya
	- K: **Dian pelari**

- Argumen pada contoh 1 dikatakan logis karena pernyataan 1 dan 2 (premis) diikuti oleh satu pernyataan berupa kesimpulan yang berasal dari premis-premisnya.
- Sedangkan pada contoh 2 akan menimbulkan perbincangan, walaupun kesimpulan tetap mengikuti premis-premisnya

## Validitas Argumen
- Validitas argumen adalah premis-premis yang diikuti oleh suatu kesimpulan yang berasal dari **premis-premisnya** dan bernilai benar.
- Validitas dapat dibedakan dengan kebenaran dari kesimpulan.
- Jika satu atau lebih premis salah, maka kesimpulan dari argument tersebut juga salah.

- Contoh 3:
	- P1: Semua mamalia adalah hewan berkaki empat.
	- P2: Semua manusia adalah mamalia.
	- K: **Semua manusia adalah hewan berkaki empat.**
- Contoh tersebut adalah argumen yang valid, tetapi dengan premis pertama yang bernilai salah.
- Argumen tersebut tetap dianggap valid, karena kesimpulannya tetap mengikuti premisnya.
- Ini merupakan **tautologi (tautology)** atau valid kebenarannya secara fungsional.

- Di lain sisi dapat terjadi suatu argumen yang tidak valid (invalid), tetapi mempunyai kesimpulan yang bernilai benar.
- Contoh 4:
	- P1: Ada makhluk hidup berkaki dua.
	- P2: Semua manusia adalah makhluk hidup.
	- K: **Semua manusia berkaki dua.**
- Argumen pada contoh tersebut tidak valid, tetapi menghasilkan kesimpulan yang benar meskipun tidak mengikuti premisnya.

- Kesimpulannya bahwa logika hanya mempermasalahkan bentuk argumen, bukan isi argumen.
- Jika suatu argumen valid, maka pokok pernyataan dapat digantikan untuk semua yang bisa dihantikannya dan v=validitas tidak terganggu.
- Namun, jika argumen tidak valid, maka akan mengganggu.
- Pada contoh tersebut, jika "berkaki dua" diganti dengan "berkaki empat" , maka akan membuat premis bernilai benar, tetapi kesimpulan bernilai salah.

## Argumen Kuat Secara Logis
- Validitas yang logis adalah hubungan antara premis dengan kesimpulan yang mempastikan bahwa jika premis-premis benar, maka hharus diikuti dengan kesimpulan yang benar dengan menggunakan aturan-aturan logika.
- **Argumen disebut kuat secara logis (sound), jika dan hanya jika argumennya valid dan semua premis-premisnya bernilai benar.**
- Contoh 5:
	- P1: Semua pekerja mendapat THR.
	- P2: Anita adalah pekerja.
	- K: **Anita mendapat THR.**
- Kesimpulan dapat bernilai benar meskipun muncul dan terlepas dari premisnua, namun tentunya ini bukan argumen yang kuat secara logis.
- Contoh 6:
	- P1: Semua siswa rajin belajar.
	- P2: Yono seorang siswa.
	- K: **Yono rajin belajar.**
- Kesimpulan di atas tidak ada hubungannya dengan premisnua, meskipun bisa bernilai benar dan premisnya juga bernilai benar. Namun jelas bukan argumen yang kuat secara logis.

- Contoh 7:
	- P1: Semua binatang dapat terbang.
	- P2: Gajah adalah binatang
	- K: **Gajah dapat terbang.**
- Argumen ini dikatakan valid, namun validitasnya tidak kuat (not sound) karena jelas premis pertama pada contoh tersebut salah.
- Walaupun argumen tersebut bisa valid, namun validitasnya tidak kuat.

## Sound Argument
- Suatu argumen logis dapat disebut kuat (sound) jika dan hanya jika memenuhi dua persyaratan berikut:
	- Argumen valid.
	- Semua premis-premisnya benar.

## Logika Matematika
Logika matematika yang menangani masalah *well-formed formulae* yang hanya memiliki nilai benar atau salah adalah:
- **Logika Proposisional** (Propositional Logic/Propositional Calculus)
	Fokus utama logika ini pada pernyataan-pernyaatn yang da[at digolongkan dalam pengertian proposisi.
- **Logika Predikat**(Predicate Logic/Predicate Calculus)
	Pernyataan yang tidak dapat digolongkan sebagai proposisi, dan tidak dapat diproses dengan logika proposisional, akan ditangani logika predikat yang memfokuskan diri pada predikat yang selalu menyertai suatu pernyataan dalam bentuk kalimat.