# Kalkulator Deret

Satu file HTML (`kalkulator-deret.html`) untuk mengerjakan soal deret angka dan deret huruf, seperti di tes penalaran numerik, TPA, psikotes, dan tes seleksi. Tidak perlu instalasi dan tidak butuh internet untuk menghitung. Buka file di browser, pilih **Angka** atau **Huruf**, lalu ketik deretnya.

## Yang bisa dilakukan

1. **Mencari suku berikutnya.** Ketik `2, 6, 12, 20, 30, ?` dan kalkulator menjawab `42`. Untuk huruf, `A, C, E, G, ?` dijawab `I`.
2. **Mencari suku yang hilang di tengah deret.** Ketik `1, 2, 4, 7, ?, 16` dan kalkulator menjawab `11`. Untuk huruf, `B, D, ?, H, J` dijawab `F`.
3. **Menampilkan langkah pengerjaan** dalam bahasa Indonesia, lengkap dengan rumus pola.
4. **Menampilkan tabel selisih** seperti coretan di kertas ujian. Suku hasil hitungan diberi latar berwarna.
5. **Menghitung beberapa suku ke depan.** Pilih 1, 3, atau 5 suku berikutnya.
6. **Menampilkan kemungkinan pola lain** kalau lebih dari satu pola cocok dengan yang dimasukkan. Jawaban utama memakai pola yang paling umum keluar di soal.
7. **Mengenali jenis deret otomatis.** Kalau kamu mengetik huruf saat mode Angka aktif (atau sebaliknya), kalkulator pindah mode sendiri.
8. **Contoh soal siap klik** untuk tiap jenis pola.

## Cara memakai

- Pilih **Angka** atau **Huruf** di bagian atas.
- Pisahkan suku dengan koma atau spasi: `3, 6, 12, 24, ?` atau `3 6 12 24 ?`.
- Tanda suku yang dicari: `?`. Pakai satu tanda saja. Untuk deret angka, `x` dan `_` juga diterima.
- Minimal 3 suku.
- Tekan **Hitung** atau Enter.

## Deret angka: pola yang dikenali

| Pola | Contoh | Jawaban |
|---|---|---|
| Aritmetika (beda tetap) | `5, 8, 11, 14, ?` | 17 |
| Geometri (rasio tetap) | `3, 6, 12, 24, ?` | 48 |
| Bilangan kuadrat dan kubik (pokoknya boleh aritmetika, geometri, atau prima) | `1, 4, 9, 16, ?` | 25 |
| Selisih bertingkat (selisih tingkat 2 atau 3 yang tetap) | `2, 6, 12, 20, 30, ?` | 42 |
| Selisih membentuk deret geometri | `3, 5, 9, 17, ?` | 33 |
| Pengali naik teratur | `1, 2, 6, 24, ?` | 120 |
| Fibonacci (jumlah dua suku sebelumnya) | `2, 3, 5, 8, 13, ?` | 21 |
| Jumlah tiga suku sebelumnya | `1, 2, 4, 7, 13, 24, ?` | 44 |
| Bilangan prima berurutan | `2, 3, 5, 7, 11, ?` | 13 |
| Kalikan lalu tambah (misalnya ×2 + 1) | `2, 5, 11, 23, ?` | 47 |
| Dua operasi bergantian | `5, 10, 8, 16, 14, ?` | 28 |
| Dua deret bersilang (suku ganjil dan genap punya pola sendiri) | `1, 5, 2, 10, 3, 15, ?` | 4 |
| Angka tetap | `7, 7, 7, ?` | 7 |

## Deret huruf: pola yang dikenali

Huruf diubah ke nomor urut alfabet (A = 1 sampai Z = 26). Alfabet berputar: setelah Z kembali ke A, dan sebelum A kembali ke Z. Di bawah hasil ada strip nomor urut A sampai Z dengan jawaban yang disorot.

| Pola | Contoh | Jawaban |
|---|---|---|
| Loncat maju dengan langkah tetap | `A, C, E, G, ?` | I |
| Loncat mundur dengan langkah tetap | `Z, X, V, T, ?` | R |
| Loncat melewati Z (berputar) | `X, Z, B, D, ?` | F |
| Loncatan berubah teratur | `A, B, D, G, K, ?` | P |
| Dua deret bersilang | `A, Z, B, Y, C, X, ?` | D |
| Dua loncatan bergantian | `A, C, D, F, G, ?` | I |
| Hanya huruf vokal (A, E, I, O, U) | `A, E, I, O, ?` | U |
| Hanya huruf konsonan | `B, C, D, F, G, ?` | H |
| Pola berulang | `A, B, C, A, B, C, A, ?` | B |
| Huruf berulang | `M, M, M, ?` | M |

**Suku berisi beberapa huruf.** Tiap posisi huruf diperlakukan sebagai deret sendiri.

| Contoh | Jawaban |
|---|---|
| `AB, CD, EF, GH, ?` | IJ |
| `ABC, BCD, CDE, ?` | DEF |

Cara menulis deret huruf:

- Pisahkan dengan koma atau spasi: `A, C, E, G, ?`
- Atau tulis rapat tanpa pemisah: `ACEG?`
- Huruf besar dan kecil sama saja.
- Dalam mode Huruf, `X` dibaca sebagai huruf X. Tanda yang dicari hanya `?` atau `_`.
- Suku berisi beberapa huruf harus sama panjang, maksimal 6 huruf.

## Batasan

- Soal campuran huruf dan angka (misalnya `A1, B2, C3`) belum didukung.
- Pola yang tidak ada di daftar di atas dijawab "Pola belum ketemu". Menambah beberapa suku sering membantu.
- Dengan suku yang sedikit, beberapa pola bisa cocok sekaligus. Cek bagian **Kemungkinan lain** dan pilih yang paling masuk akal untuk soalnya.
- Jumlah suku minimum bervariasi per pola. Selisih bertingkat tingkat 2 butuh 4 suku, tingkat 3 butuh 5 suku, dua deret bersilang butuh 5 sampai 6 suku.
- Untuk angka yang hilang di tengah, kalkulator mencoba bilangan bulat dalam rentang sekitar 50 kali angka terbesar di deret. Jawaban desimal tidak dicari.
- Hasil angka di atas 10^15 tidak ditampilkan.
- Untuk deret huruf dengan beberapa huruf per suku, kemungkinan pola lain tidak ditampilkan.

## Teknis

- Satu file HTML, tanpa framework dan tanpa library. Perhitungan berjalan di browser.
- Font dimuat dari Google Fonts. Kalau offline, tampilan memakai font bawaan sistem dan hitungan tetap jalan.
- Tema terang dan gelap mengikuti pengaturan perangkat.
- 
