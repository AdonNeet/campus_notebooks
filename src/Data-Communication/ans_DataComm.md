<h1 style="font-size: 28px"> Komunikasi Data </h1>

<h2 style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 100%"># Data Transmisi</h2>

<h2 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] Terminologi Transmisi</h2>

- Transmisi data terjadi antara pemancar dan penerima melalui beberapa media
- Guided medium (Media yang dipandu)
>	Ex: twisted pair(kabel berpasangan), coaxial cable (kabel koaksial), optical fiber (fiber optik)
- Unguided/wireless medium
>	Ex: udara, air, ruang hampa

<h2 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] Konfigurasi yang mungkin</h2>

\> Direct link
- Tidak ada perangkat perantara
\> Point-to-Point
- Hanya 2 perangkat yang berbagi link
\> Multi-Point
- Lebih dari dua perangkat yang berbagi link

<h2 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] Arah komunikasi/transmisi</h2>

\> Simplex
Satu arah
>	Ex: Broadcasting televsi-radio

\> Half Duplex
Dua arah, tetapi hanya satu arah pada satu waktu (penggunaan kanal bergantian)
>	Ex: Handy Talky (HT)

\> Full Duplex
Dua arah secara bersamaan
>	Ex: telepon

<h2 style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 100%"># OSI-TCP/IP Layer</h2>

<h3 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] TCP/IP Layers</h3>

Tidak ada model resmi tetapi yang utamanya berfungsi:
- Application Layer
- Host-to-host atau transport layer
- Internet layer
- Network access layer
- Physical layer

<b> &nbsp; > Physical Layer</b>
>	Berkaitan dengan antarmuka (interface) fisik antara komputer dan jaringan.

Berkaitan dengan masalah seperti:
- Karakteristik media transmisi
- Level sinyal
- Kecepatan data
- Hal-hal terkait lainnya

<b> &nbsp; > Network Access Layer</b>
>	Pertukaran data antara sistem akhir dan jaringan terpasang.

Berkaitan dengan masalah seperti:
- Penyediaan alamat tujuan
- Pemanggilan layanan tertentu seperti prioritas
- Akses ke & merutekan data melalui link jaringan antara dua sistem yang terhubung

Ini memungkinkan lapisan di atas mengabaikan link spesifik.

<b> &nbsp; > Internet Layer (IP)</b>
>	Fungsi perutean di beberapa jaringan 

Untuk sistem yang terhubung ke jaringan yang berbeda menggunakan protokol IP, diimplementasikan di sistem akhir dan router
>	Router menghubungkan dua jaringan dan menyampaikan data di antara mereka

<b> &nbsp; > Transport Layer (TCP)</b>
>	Lapisan umum yang digunakan bersama oleh semua aplikasi

Menyediakan pengiriman data yang handal dalam urutan yang sama seperti yang dikirim. Biasanya menggunakan TCP.

<b> &nbsp; > Application Layer</b>
>	Memberikan dukungan untuk aplikasi pengguna

Membutuhkan modal terpisah untuk setiap jenis aplikasi

<h3 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] OSI Layers</h3>

>	Open System Interconnection
>	-> Merupakan sistem teoritis disampaikan
>	-> TCP/IP adalah standar de facto

Memiliki 7 lapisan:
- Application layer
- Presentation layer
- Session layer
- Transport layer
- Network layer
- Data link layer
- Physical layer

<b> &nbsp; > Application Layer</b>
Memberikan akses ke lingkungan OSI untuk pengguna dan juga menyediakan layanan informasi terdistribusi

<b> &nbsp; > Presentation Layer</b>
Memberikan kemandirian(?) pada proses aplikasi dari perbedaan representasi data (sintaks)

<b> &nbsp; > Session Layer</b>
>	-> Menyediakan struktur kontrol untuk komunikasi antar aplikasi
>	-> Menetapkan, mengelola dan mengkahiri koneksi (sesi) antara aplikasi yang bekerja sama

<b> &nbsp; > Transport Layer</b>
>	-> Menyediakan transfer data yang andal dan transparan antar titik akhir
>	-> Menyediakan pemulihan kesalahan ujung ke ujung dan kontrol aliran

<b> &nbsp; > Network Layer</b>
>	-> Memberikan lapisan atas kemandirian(?) dari transmisi data dan teknologi switching yang digunakan untuk menghubungkan sistem
>	-> Bertanggung jawab untuk membangun, memelihara, dan mengakhiri koneksi

<b> &nbsp; > Data Link Layer</b>
>	-> Menyediakan transfer informasi yang andal melalui tautan fisik
>	-> Mengirimkan blok (bingkai) dengan sinkronisasi yang diperlukan, kontrol kesalahan, dan kontrol aliran

<b> &nbsp; > Physical Layer</b>
>	-> Berkaitan dengan transmisi aliran bit tidak tersturktur melalui media fisik
>	-> Berkaitan dengan karakteristik mekanik, listirk, fungsional, dan prosedural untuk mengakses media fisik

<h3 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] OSI vs TCP/IP Layers</h3>

<br></br>

<center>
<table style="border: 1px solid lightgray;">
	<tr>
		<th width="250px" align="center">OSI</th>
		<th width="250px" align="center">TCP/IP</th>
	</tr>
    <tr>
	    <td align="center">Application</td>
        <td align="center" rowspan="3">Application</td>
    </tr>
    <tr>
        <td align="center">Presentation</td>
    </tr>
    <tr>
	    <td align="center"> &nbsp; </td>
    </tr>
    <tr>
	    <td align="center">Session</td>
	    <td align="center" rowspan="2">Transport (Host-to-host)</td>
    </tr>
    <tr>
	    <td align="center">Transport</td>
    </tr>
    <tr>
	    <td align="center" rowspan="2">Network</td>
	    <td align="center">Internet</td>
    </tr>
    <tr>
	    <td align="center"> &nbsp; </td>
    </tr>
    <tr>
	    <td align="center"> &nbsp; </td>
		<td align="center" rowspan="2">Network Access</td>
    </tr>
    <tr>
	    <td align="center">Data Link</td>
    </tr>
    <tr>
	    <td align="center">Physical</td>
	    <td align="center">Physical</td>
    </tr>
</table>
</center>

<!--

<h3 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] Model Komunikasi</h3>



<h3 style="margin-bottom: 1px; border-bottom: 2px dashed grey; display: inline-block; width: 75%">[>_] Teknik Pengkodean Sinyal</h3>


<b> &nbsp; > Manchester Diferensial</b>
--> 