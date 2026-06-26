# 📺 Regression Intro - Practical Machine Learning Tutorial with Python p.2 oleh Sentdex <br>[Sentdex](https://youtu.be/JcI5Vnw0b2c?si=Lvt5Fq59rf8Cr5Ln)

### 1. Pengenalan Konsep Dasar Regresi

Video ini menjelaskan dasar-dasar regresi linear dalam konteks supervised machine learning.

- **Tujuan Regresi:** Memodelkan data kontinu dengan mencari garis best-fit (garis lurus) melalui data tersebut.

- **Fitur vs Label:** Dalam machine learning, data dibagi menjadi fitur (atribut/input) dan label (hasil yang ingin diprediksi).

---

### 2. Pengolahan Data Saham

Sentdex menggunakan data harga saham sebagai contoh karena sifat datanya yang kontinu.

- **Pentingnya Fitur yang Bermakna:** Tidak semua data mentah (Open, High, Low, Close) diperlukan. Menggunakan terlalu banyak fitur yang berlebihan dapat menghambat performa model sederhana.

- **Data Adjusted:** Penjelasan mengapa harga adjusted (penyesuaian) lebih penting digunakan daripada harga mentah, terutama untuk menangani peristiwa seperti stock splits.

---

### 3. Teknik Feature Engineering

Agar model linear sederhana bisa menangkap hubungan antar data, kita perlu membuat fitur baru yang lebih informatif daripada sekadar harga mentah:

- **High-Low Percentage (Volatilitas):** Dihitung dari selisih harga tertinggi dan terendah sebagai proksi volatilitas harian.

- **Percentage Change (Momentum Harian):** Dihitung dari selisih harga penutupan dan pembukaan untuk melihat pergerakan harga harian.

- **Volume:** Tetap dipertahankan karena memiliki hubungan dengan volatilitas.

---

### Langkah Selanjutnya

Di akhir video, ditekankan bahwa pemilihan fitur adalah tahap kritis. Penonton diajak untuk berpikir "apakah harga adjusted close yang ada saat ini nantinya akan berfungsi sebagai fitur atau justru menjadi target label yang ingin diprediksi di masa depan ?".

---

_Video Referensi_: [Regression Intro - Practical Machine Learning Tutorial with Python p.2](https://youtu.be/JcI5Vnw0b2c?si=Lvt5Fq59rf8Cr5Ln)
