# TryHackMe: Inside a Computer

- Platform: TryHackMe
- Difficulty: Info / Easy
- Category: Pre-Security > Hardware Details
- Date Completed: 5 November 2026

---

## Executive Summary

Room ini memberikan simulasi interaktif tentang komponen hardware internal komputer, fungsi dasar dari setiap komponen hardware, serta dampaknya terhadap sistem jika komponen penting tidak terpasang atau mengalami kegagalan fungsi.

---

## Key Concepts & Notes

- Motherboard: Papan sirkuit utama yang menghubungkan seluruh komponen hardware komputer agar dapat saling berkomunikasi.
- Power Supply Unit (PSU): Komponen yang mengonversi dan mendistribusikan daya listrik ke seluruh bagian sistem komputer.
- Central Processing Unit (CPU): Otak komputer yang memproses seluruh instruksi dan perhitungan data. Jika CPU tidak ada atau rusak, sistem komputer tidak akan bisa melakukan boot.
- Graphics Processing Unit (GPU): Komponen khusus yang bertugas merender gambar dan output visual ke layar monitor.

---

## Step-by-Step & Analysis

### Task 1 & Interactive Lab - Reassembling the Machine

- Melakukan perakitan komponen internal komputer pada lab 3D simulasi.
- Mengidentifikasi komponen yang diperlukan dan mengabaikan komponen non-esensial/distraksi yang tidak perlu dipasang (seperti HDD sekunder, GPU eksternal laptop, Wi-Fi dongle tambahan, dan adaptor daya yang tidak sesuai).
- Mengakses folder EvidenceViewer setelah sistem berhasil merakit dan melakukan boot sequence.

### Task 2 - Hardware Verification & Quiz

1. Function of GPU:
   - Jawaban: Renders images and visual output to the screen
2. Function of Power Supply Unit (PSU):
   - Jawaban: Convert main electricity into the voltage each component needs
3. What happens if the CPU is missing:
   - Jawaban: Nothing executes - the machine cannot function at all
4. Function of Motherboard:
   - Jawaban: It connects and routes communication between all components

### Task 3 - Flag Recovery

- Menyelesaikan seluruh verifikasi penemuan bukti pada modul Evidence Viewer.
- Mendapatkan laporan Forensic Recovery Report dan mengirimkan hasil analisis ke Senior Analyst.
- Flag / Answer: THM{c0ld_b00t_c0mpl3t3}

---

## Lessons Learned & Reflection

- Memahami struktur fisik hardware komputer yang menjadi tempat berjalannya sistem operasi dan perangkat lunak.
- Mengetahui fungsi inti dari masing-masing komponen hardware (CPU, PSU, GPU, Motherboard) dalam mendukung operasional sistem secara menyeluruh.
