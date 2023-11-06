<h1 style="font-size: 28px"> Teori Bahasa dan Automata </h1>

<h2 style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 100%"># Introduction</h2>

[>\_] Ada beberapa <u>tingkatan bahasa Pemrograman</u>, antara lain:
- Bahasa tingkat rendah &nbsp;&nbsp;  -> Bahasa Mesin
- Bahasa tingkat menengah &nbsp;-> Bahasa Assembly
- Bahasa tingkat tinggi &nbsp;&nbsp; -> Bahasa java, Python, PHP, dll

[>\_] Lalu, <u>bagaimana sebuah mesin dapat memahami kode program yang dibuat oleh programmer</u>?

>	Sebuah mesin yang hanya mengenali bahasa mesin dapat memahami bahasa pemrograman tingkat tinggi karena adanya Compiler (kompilator/penerjemah)

<b>Teori Bahasa dan Automata adalah dasar dari teknik Kompilasi</b>

[>_] Apa yang dimaksud Teori Bahasa dan Automata?
- Automata adalah mesin abstrak yang dapat mengenali (recognize), menerima (accept), atau membangkitkan  (generate) sebuah kalimat dalam bahasa tertentu.
- Input pada mesin automata dianggap sebagai bahasa yang harus dikenali oleh mesin.
- Mesin akan mengindikasikan apakah suatu bahasa dapat diterima atau tidak.

[>\_] Mesin automata sederhana
```mermaid
%%{init: {'theme':'light', 'themeCSS': 'svg {background-color: black}'}}%%
flowchart LR
	x( ) --> 0((Q_0)) -- a --> 1((Q_1)) -- d --> 2((Q_2)) -- a --> 3(((Q_3)))
	2 -- d --> 5((Q_5))
	2 -- u --> 4(((Q_4)))
	4 ~~~ 5
```
- 6 state {q0, q1, q2, q3, q4, q5}
- Initial state {q0}
- Final state {q3, q4}
- Simbol input {a, d, u}

Note:
- String input diterima jika mencapai final state, selain itu ditolak
- Pembacaan simbol pertama dimulai dari initial state
- Perpindahan state berdasarkan simbol yang dibaca

```mermaid
%%{init: {'theme':'light', 'themeCSS': 'svg {background-color: black}'}}%%
flowchart LR
	x( ) --> 0((Q_0)) -- a --> 1((Q_1)) -- d --> 2((Q_2)) -- a --> 3(((Q_3)))
	2 -- d --> 5((Q_5))
	2 -- u --> 4(((Q_4)))
	4 ~~~ 5
```
Input String:
- ada = diterima
- adu = diterima
- add = ditolak

<h2 style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 100%"># Simbol, String, dan Bahasa</h2>

[>\_] Apa itu simbol?
>	Suatu entitas abstrak yang tidak didefinisikan secara formal
>	- Bayangkan sapi
>	- Definisi "1" atau "A"

[>\_] Apa itu string?
>	String/kata/untai merupakan suatu deretan berhingga dari simbol-simbol

<center>
<table>
<tr>
	<td><center><u>a</u></center></td>
	<td><center><u>abcd</u></center></td>
</tr>
<tr>
	<td>Simbol</td>
	<td>String</td>
</tr>
</table>
</center>

>	Beberapa simbol yang membentuk string tersebut
<center>
W = <u>abbac</u> <br>
|W| = 5
</center>

Bagaimana dengan sebuah string kosong?
>	Sebuah string kosong biasanya dinyatakan dengan simbol epsilon
>	Panjangnya = 0 

$$\displaystyle \epsilon~\rightarrow~\text{String Kosong}$$


[>\_] Apa itu bahasa?
>	Suatu sistem yang meliputi pengekspresian gagasan, fakta, konse, termasuk sekumpulan simbol-simbol dan aturan untuk melakukan manipulasinya

>	Alphabet adalah himpunan berhingga dari symbol-symbol

>	Sebuah bahasa adalah himpunan string-string dari simbol-simbol untuk suatu alphabet
>>	Karena sebuah bahasa adalah sekumpulan dari string-string. Maka kita bisa mempunyai bahasa yang tidak mempunyai string-string, yaitu bahasa kosong yang dinotasikan seperti menuliskann notasi himpunan kosong

>	Bahasa juga bisa disebut sebagai rangkaian simbol-simbol yang memiliki makna

- Input pada mesin automata dianggap sebagai bahasa yang harus dikenali oleh mesin
- Mesin akan mengindikasikan apakah suatu bahasa dapat diterima atau tidak

<h2 style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 100%"># Tata Bahasa Hirarki Chomsky dan Aturan Produksi</h2>

[>\_] Simbol Terminal dan Non-Terminal

<b> &nbsp; > Apa itu symbol terminal?</b>
>	Symbol yang tidak dapat diturunkan lagi

&nbsp; Yang termasuk symbol terminal
- Huruf kecil alfabet, misalnya: a. b, c
- Simbol operator, misalnya: +, -, dan \*
- Simbol tanda baca, misalnya: (), dan ;
- String yang tercetak tebal, misanya: **if**, **then**, dan **else**

<b> &nbsp; > Apa itu symbol non-terminal?</b>
>	Symbol yang masih bisa diturunkan menjadi symbol Terminal atau Non-terminal lainnya

&nbsp; Yang termasuk symbol non-terminal
- Huruf besar alfabet, misalnya: A, B, C
- Huruf S sebagai symbol awal
- String yang tercetak miring. Misalnya: *expr* dan *stmt*

[>\_] Aturan Produksi

Aturan produksi dinyatakan dalam:

<center>

| | | |
|-|-|-|
| Alpha menyatakan<br>symbol-symbol<br>pada ruas kiri aturan<br>produksi| $$\displaystyle \alpha \rightarrow \beta$$ | Beta Menyatakan<br>symbol-symbol<br>pada ruas kanan<br>aturan produksi|
| | | |

Dibaca alpha menurunkan beta atau alpha menghasilkan beta<br>Simbol dapat berupa symbol terminal atau non-terminal
</center>

- Dengan menerapkan aturan produksi, suatu tata bahasa bisa menghasilkan sejumlah string
- Himpunan semua string tersebbut adalah bahasa yang didefinisikan oleh tata bahasa tersebut

Contoh aturan produksi
$$\displaystyle T \rightarrow a$$
$$\displaystyle E \rightarrow T~|~T + E$$

[>\_] Hirarki Chomsky

>	Hirarki Chomsky merupakan pembagian tingkatan bahasa yang dibatasi oleh aturan produksi masing-masing

>	Noam Chomsky membagi tingkatan bahasa menjadi 4


&nbsp; 4 Tingkatan tata Bahasa menurut Chomsky
- Tipe 0 - Unrestricted Grammar (Bahasa Unrestricted)
- Tipe 1 - Context Sensitive Grammar (Bahasa Context Sensitive)
- Tipe 2 - Context Free Grammar (Bahasa Bebas Konteks)
- Tipe 3 - Regular Grammar (Bahasa Reguler)


<b style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 65%"> &nbsp; > Bahasa Unrestricted</b>

>	Bahasa unrestricted (Phase Structure/ Natural Language/ Type 0) berkaitan dengan Mesin Turing
>>	Bahasa ini dikatakan Bahasa natural karena sudah termasuk bahasa yang dapat dimengerti oleh manusia
>	Aturan produksinya sebagai berikut:

- Aturan produksi pada ruas kiri $(\alpha)$ harus memiliki minimal sebuah simbol variable/non-terminal dan tidak boleh kosong.
- Aturan produksi ruas kanan $(\beta)$ rangkaian symbol terminal dan non-terminal

&nbsp;  <b>Contoh</b>

| Tata bahasa *unrestricted* yang dapat diterima | Tata bahasa *unrestricted* yang tidak dapat diterima |
| ----- | ----- |
| Abc -> e | efg -> h |
| bCDef -> DC | ab -> $\epsilon$ |
| abEF -> Dc | |
| gHj -> $\epsilon$ | |
| | |

// minimal ruas kiri memiliki non-terminal

<b style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 65%"> &nbsp; > Bahasa Context Sensitive</b>
>	Bahasa context sensitive (Type 1) merupakan tata bahasa yang berkaitan dengan mesin Linear Bounded Automata
>	
>	Aturan produksinya sebagai berikut:

- Aturan produksi ruas kiri $(\alpha)$ minimal harus memiliki sebuah variable (non-terminal)
- Jumlah string pada  ruas kiri harus <u>lebih kecil sama dengan</u> jumlah string pada ruas kanan. Secara matematika dapat dituliskan $|\alpha|\leq|\beta|$

&nbsp;  <b>Contoh</b>

| Tata bahasa *context sensitive* yang dapat diterima | Tata bahasa *context sensitive* yang tidak dapat diterima |
| ----- | ----- |
| A -> ec | s -> h |
| Ab -> ef | Sab -> Cd |
| AC -> FG | AACD -> ef |
| sA -> cDF | CD -> $\epsilon$ |
| EF -> AbGh | scG -> $\epsilon$ |
| B -> $\epsilon$ | |
| | |

// minimal ruas kiri memiliki non terminal dan $|\alpha|\leq|\beta|$

&nbsp;  <b><u>Catatan:</u></b>
Pada tata bahasa *context sensitive* (syarat: $|\alpha|\leq|\beta|$)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $B\rightarrow\epsilon$ **(dapat diterima)**
Aturan produksi di atas daianggap dapa tditerima oleh mesin automata, karena *context sensitive* hanya menghitung jumlah string ruas kiri dan kanan, dimana:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $|B|=1,|\epsilon|=1$
Sehingga $B\rightarrow\epsilon$ dianggap memenuhi aturan produksi context sensitive.

<b style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 65%"> &nbsp; > Bahasa Context Free</b>

>	Bahasa bebas konteks (Type 2) merupakan tata bahasa yang berkaitan dengan mesin Push Down Automata (PDA)
>	
>	Aturan produksinya sebagai berikut:

- Aturan produksi hampir sama dengan tipe 0 tapi ruas kiri $(\alpha)$ hanya memiliki sebuah simbol variable (non-terminal). // hanya satu digit, yaitu non-terminal saja
- Aturan produksi ruas kanan $(\beta)$ tidak memiliki Batasan (terminal/non-terminal/epsilon)

&nbsp;  <b>Contoh</b>

| Tata bahasa *context free* yang dapat diterima | Tata bahasa *context free* yang tidak dapat diterima |
| ----- | ----- |
| A ->  c | a -> Cd |
| B -> cD | Aa -> c |
| S -> Ad | CD -> f |
| C -> AAA | $\epsilon$ -> aB |
| S -> $\epsilon$ | |
| | |

// ruas kiri hanya memiliki satu digit, yaitu non-terminal

<b style="margin-bottom: 5px; border-bottom: 2px solid grey; display: inline-block; width: 65%"> &nbsp; > Bahasa Regular</b>

>	Bahasa reguler (Type 3) merupakan tata bahasa yang berkaitan dengan mesin Finite State Automata (FSA).
>	
>	Aturan produksinya sebagai berikut:

- Aturan produksi ruas kiri $(\alpha)$ harus memiliki sebuah simbol variable/non-terminal. // hanya 1 digit, yaitu non-terminal
- Aturan pproduksi ruas kanan $(\beta)$ maksimal memiliki sebuah simbol variabel (apabila ada, harus terletak di posisi paling kanan). // hanya ada 1 non-terimnal, terletak di pojok kanan di sampin terminal


&nbsp;  <b>Contoh</b>

| Tata bahasa *regular* yang dapat diterima | Tata bahasa *regular* yang tidak dapat diterima |
| ----- | ----- |
| S -> a | s -> a |
| S -> A | As -> c |
| S ->  cD | C -> Bd |
| S -> efG | C -> aBD |
|  |  $\epsilon$ -> bdC |
| | |

// ruas kiri hanya memiliki satu digit, yaitu non-terminal
// non-terminal pada ruas kanan terletak di pojok kanan

&nbsp;  <b><u>Catatan:</u></b>
Pada tata bahasa regular, ruas kiri haruslah sebuah variable 
(1 digit non-terminal)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $\epsilon$ -> bdC **(tidak dapat diterima)**
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; S -> $\epsilon$ **(diperbolehkan jika S tidak muncul di ruas kanan)**
Aturan produksi di atas dianggap tidak dapat diterima oleh mesin automata, karena $\epsilon$ tidak dapat menuruknan aturan produksi apapun dan dianggap tidak memenuhi persyaratan aturan produksi tata bahasa regular.

\[WORK IN PROGRESS\]


