# TryHackMe: Offensive Security Intro

- **Platform:** TryHackMe
- **Difficulty:** Info / Easy
- **Category:** Pre-Security
- **Date Completed:** 2 November 2026

---

## Executive Summary
Room ini memberikan pengenalan dasar tentang cara kerja simulasi peretasan (Offensive Security), penggunaan terminal di Linux, serta dasar enumerasi web menggunakan tool DIRB untuk menemukan direktori tersembunyi.

---

## Key Concepts & Notes
* **Directory Enumeration:** Proses mencari halaman atau direktori tersembunyi pada web server yang tidak tampil di navigasi utama.
* **HTTP Status Code:**
  * `200 OK`: Halaman ditemukan dan berhasil diakses.
  * `301 Moved Permanently`: Halaman dialihkan (redirect).
* **DIRB Tool:** Tool CLI berbasis brute-force wordlist untuk melakukan enumerasi direktori web.

---

## Step-by-Step & Analysis

### Task 1 - Think like a Hacker!
- Mengenal pola pikir peretas (offensive security) dan bagaimana cara menganalisis sistem target dari sudut pandang penyerang.

### Task 2 - Starting the Lab
- Menjalankan mesin virtual / lab interaktif di TryHackMe untuk mengakses browser dan terminal latihan.

### Task 3 - Find Hidden Pages
- **Command:** `dirb http://fakebank.thm`
- **Hasil Scanning:**
  ```text
  + [http://fakebank.thm/bank-transfer](http://fakebank.thm/bank-transfer) (CODE:200|SIZE:4663)
  + [http://fakebank.thm/images](http://fakebank.thm/images) (CODE:301|SIZE:179)

### Task 4 - Attack the Admin Page
- Menambahkan /bank-transfer pada URL browser untuk mengakses halaman transfer tersembunyi.
- Memasukkan nomor akun 8881 dan melakukan transfer sebesar $2000 untuk mengubah saldo akun dari negatif menjadi positif.
- Flag / Answer: BANK-HACKED

---

## Lessons Learned & Reflection
- Memahami bahwa halaman web yang tidak dipajang di menu utama belum tentu aman jika tidak diberikan proteksi autentikasi yang tepat.
- Mengetahui cara kerja dasar enumerasi web menggunakan DIRB.
