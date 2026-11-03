# TryHackMe: Defensive Security Intro

- **Platform:** TryHackMe
- **Difficulty:** Info / Easy
- **Category:** Pre-Security > Introduction to Cyber Security
- **Date Completed:** 3 November 2026

---

## Executive Summary

Room ini memberikan pengenalan dasar mengenai sudut pandang tim penahan (_Defensive Security / Blue Team_). Fokus utamanya adalah memahami alur kerja _SOC Analyst_ dalam memantau _dashboard monitoring_, mengidentifikasi aktivitas mencurigakan (_Web Discovery Attack_), menganalisis IP penyerang, dan melakukan _containment_ (pemblokiran IP) menggunakan Firewall.

---

## Key Concepts & Notes

- **Defensive Security Goal:** Mendeteksi dan merespons serangan (_detect and respond_) sebelum dampak kerusakan terjadi pada sistem.
- **SOC Monitoring Dashboard:** Antarmuka yang digunakan analis keamanan untuk memantau trafik jaringan, peringatan (_alerts_), dan pola aktivitas mencurigakan secara _real-time_.
- **Web Discovery Attack:** Upaya enumerasi otomatis dari pihak luar untuk menemukan titik masuk/halaman sensitif pada web server.
- **IP Blocking & Incident Response:** Tindakan mitigasi cepat dengan memblokir alamat IP penyerang pada sistem _Firewall_ guna menghentikan akses lebih lanjut.

---

## Step-by-Step & Analysis

### Task 1 - Think like a Defender

- Memahami konsep dasar keamanan defensif di mana fokus utamanya adalah memantau, mendeteksi, dan merespons ancaman, bukan menyerang sistem.
- **Jawaban:** `Detect and respond to attacks`

### Task 2 - Detect Suspicious Activity

- Membuka _Security Analyst Dashboard_ untuk meninjau _alert_ yang masuk.
- Menganalisis _event_ bertipe **Web Discovery Attack** dan mengidentifikasi IP penyerang yang melakukan enumerasi pada endpoint admin.
- **Jawaban (Source IP):** `32.122.195.63`

### Task 3 - Identify the Attack

- Memeriksa daftar _URL Discovery Attempts_ pada dashboard untuk melihat pola percobaannya.
- Menemukan percobaan akses halaman sensitif terbaru yang dicoba oleh penyerang (`https://fakebank.com/admin`).
- **Jawaban (Latest URL):** `https://fakebank.com/admin`

### Task 4 - Stop the Attack

- Membuka menu _Implement Security Actions / Firewall Manager_.
- Memasukkan IP penyerang (`32.122.195.63`), memilih aksi **BLOCK**, lalu mengaplikasikan aturan firewall baru.
- Berhasil menghentikan lalu lintas serangan dan mendapatkan flag mitigasi.
- **Flag / Answer:** `THM{FAKEBANK-SECURED}`

---

## Lessons Learned & Reflection

- Memahami peran penting _monitoring dashboard_ bagi seorang _SOC Analyst_ dalam mengenali anomali lalu lintas jaringan.
- Mempelajari alur _Incident Response_ dasar: **Detect** (Deteksi IP) ➡️ **Identify** (Analisis pola serangan/URL) ➡️ **Contain/Stop** (Terapkan aturan Blokir di Firewall).
