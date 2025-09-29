Nama: Anggriani Hermawan
NIM: 312410175
Kelas: TI.24.A2

Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 140130" src="https://github.com/user-attachments/assets/664a5f0b-e7ca-412b-95e2-69c13bd761ca" />

2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!
- h1 { ... } → selector elemen. Semua tag <h1> di halaman HTML akan mendapat gaya yang sama.
- #intro h1 { ... } → selector ID + elemen. Hanya <h1> yang berada di dalam elemen dengan id="intro" yang akan dipengaruhi.
Jadi h1 {} berlaku global untuk semua <h1>, sedangkan #intro h1 {} lebih spesifik dan hanya berlaku di dalam elemen dengan id="intro".

3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!
Ada urutan prioritas CSS yang disebut CSS Specificity dan Cascade:
1. Inline CSS → paling kuat (langsung di atribut elemen).
2. Internal CSS (di <style> ... </style> dalam file HTML).
3. Eksternal CSS (file .css yang dilink dengan <link rel="stylesheet">).
Jadi, jika ketiganya mendeklarasikan gaya untuk elemen yang sama, Inline CSS yang akan ditampilkan di browser.
Contohnya:
<head>
  <link rel="stylesheet" href="style.css"> <!-- Eksternal -->
  <style>
    p { color: green; } /* Internal */
  </style>
</head>
<body>
  <p style="color: red;">Teks Contoh</p> <!-- Inline -->
</body>
Hasil: Tulisan "Teks Contoh" berwarna merah karena inline CSS menang.
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
- ID selector (#paragraf-1) punya prioritas lebih tinggi daripada Class selector (.text-paragraf).
- Jika ada konflik gaya, maka CSS pada ID yang ditampilkan browser.
Contohnya:
