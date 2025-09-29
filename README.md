## Nama: Anggriani Hermawan
## NIM: 312410175
## Kelas: TI.24.A2

    Pertanyaan dan Tugas
    1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
    dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
    Jawab:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 140130" src="https://github.com/user-attachments/assets/b068020f-4833-411f-902c-0f0e842eebaa" />

    2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
    penjelasannya!
    Jawab:
    - h1 { ... } → selector elemen. Semua tag <h1> di halaman HTML akan mendapat gaya yang sama.
    - #intro h1 { ... } → selector ID + elemen. Hanya <h1> yang berada di dalam elemen dengan id="intro" yang akan dipengaruhi.
    Jadi h1 {} berlaku global untuk semua <h1>, sedangkan #intro h1 {} lebih spesifik dan hanya berlaku di dalam elemen dengan id="intro".
        
    3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
    elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
    penjelasan dan contohnya!
    Jawab:
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
    
    5. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
    terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
    Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
    Jawab:
    - ID selector (#paragraf-1) punya prioritas lebih tinggi daripada Class selector (.text-paragraf).
    - Jika ada konflik gaya, maka CSS pada ID yang ditampilkan browser.
    Contohnya:
    html:
    <p id="paragraf-1" class="text-paragraf">Ini contoh paragraf</p>
    css:
    .text-paragraf { color: blue; }  /* Class */
    #paragraf-1 { color: red; }      /* ID */
    Hasil: Paragraf berwarna merah karena ID lebih spesifik dibanding Class.
    
    Tuliskan penjelasan dari setiap langkah praktikum beserta screenshotnya:
    1. Membuat dokumen HTML
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 132137" src="https://github.com/user-attachments/assets/0814bc97-ea0f-4d5b-95bb-1fc0d8dd3e42" />
    
    Penjelasan:
    Belum ada styling khusus selain bawaan browser. Heading <h1> masih hitam default, link berwarna biru dengan underline, dan teks paragraf juga default hitam.
    Ini menunjukkan tampilan dasar HTML tanpa CSS tambahan.
    
    2. Mendeklarasikan CSS Internal
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 132221" src="https://github.com/user-attachments/assets/e907d4f6-b4c4-4395-af52-3b877db78a5f" />
    
    Penjelasan:
    Heading sudah berubah warna biru dan rata tengah (text-align: center;). Ada tambahan style pada teks (italic) dan link terlihat lebih rapi.
    Ini bukti CSS eksternal atau internal mulai bekerja untuk mengatur layout dasar.
    
    3. Menambahkan Inline CSS
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 133527" src="https://github.com/user-attachments/assets/3bead8b9-74e1-430a-9ac6-bbe5523650fb" />
    
    Penjelasan:
    Paragraf menjadi abu-abu (color: gray;) sementara heading tetap biru.
    Perubahan ini terjadi karena internal CSS menimpa aturan eksternal (cascade).
    
    4. Membuat CSS Eksternal
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 134813" src="https://github.com/user-attachments/assets/6069f1f2-0683-4605-bd35-eac62cf7f431" />
    
    Penjelasan:
    Navigasi di bagian atas sudah memiliki background hijau dengan link horizontal.
    Artinya aturan dari CSS eksternal lebih dominan pada bagian struktur navigasi.
    
    5. Menambahkan CSS Selector
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 135000" src="https://github.com/user-attachments/assets/ed03feaa-ef21-43e8-be69-7c909755139d" />

    Penjelasan:
    Kontainer konten (judul + paragraf) diberi background biru muda (cyan), tombol link menjadi merah dengan teks putih.
    Ini kombinasi eksternal + internal CSS, menunjukkan bahwa style dapat saling melengkapi.

    Merubah dan mengganti warna
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 135548" src="https://github.com/user-attachments/assets/4d8d3212-a9b7-480a-b340-35fb42e710b4" />

    Penjelasan:
    Background konten berubah jadi magenta (pink terang), judul <h1> menjadi putih, dan paragraf tetap abu-abu. Tombol merah tetap muncul.
    Ini efek dari inline CSS atau aturan internal paling akhir, karena inline punya prioritas paling tinggi.
    
    KESIMPULAN:
    Setiap gambar mewakili tahapan perubahan cascade CSS:
    Gambar 1 → default HTML
    Gambar 2–4 → pengaruh CSS eksternal + internal
    Gambar 5 → kombinasi styling
    Gambar 6 → inline CSS menimpa aturan lain
