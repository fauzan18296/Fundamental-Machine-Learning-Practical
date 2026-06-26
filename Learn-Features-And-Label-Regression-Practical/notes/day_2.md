# 📺 Fitur dan Label Regresi - Tutorial Belajar Mesin Praktis dengan Python p.3 <br>[Sentdex](https://youtu.be/lN5jesocJjk?si=1aI7K1OqSQmXKKx9)

## Tujuan Utama:

Menyiapkan data agar mesin dapat belajar hubungan antara Fitur (data saat ini) dan Label (harga di masa depan).

---

### 1. Menangani Data yang Hilang (NaN)

- **Waktu:** [[03:12]](https://www.google.com/search?q=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DlN5jesocJjk%26t%3D192) - [[04:37]](https://www.google.com/search?q=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DlN5jesocJjk%26t%3D277)

- **Poin Penting:** Data yang kosong (NaN) harus ditangani karena algoritma machine learning tidak bisa memprosesnya.

- **Strategi:** Mengisi data dengan angka yang sangat jauh dari nilai normal (seperti `-99999`) menggunakan `df.fillna(-99999, inplace=True)`. Ini menjadikannya "outlier" yang diabaikan oleh algoritma, sehingga kita tidak perlu menghapus baris data dan kehilangan informasi berharga.

---

### 2. Menentukan Target Prediksi (Label)

- **Waktu:** [[04:37]](https://www.google.com/search?q=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DlN5jesocJjk%26t%3D277) - [[06:20]](https://www.google.com/search?q=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DlN5jesocJjk%26t%3D380)

- **Poin Penting:** Kita perlu mendefinisikan apa yang ingin diprediksi. Dalam tutorial ini, kita menggunakan `adj_close` (harga penyesuaian) di masa depan.

- **Strategi:** Menggunakan `math.ceil(0.01 \* len(df))` untuk menentukan seberapa jauh ke masa depan kita ingin memprediksi. Nilai `0.01` (1%) bisa diubah sesuai kebutuhan (misalnya, untuk memprediksi harga hari berikutnya).

---

### 3. Menggunakan Fungsi `shift()`

- **Waktu:** [[06:20]](https://www.google.com/search?q=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DlN5jesocJjk%26t%3D380) - [[08:45]](https://www.google.com/search?q=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DlN5jesocJjk%26t%3D525)

- **Poin Penting:** Ini adalah teknik untuk membuat kolom target (label) yang berisi data masa depan.

- **Strategi:** `df['label'] = df[forecast_column].shift(-forecast_out)`. Kode ini menggeser data ke atas, sehingga setiap baris data hari ini disejajarkan dengan harga di masa depan.

---

### 4. Pembersihan Akhir

- **Waktu:** [[08:45]]() - [[09:30]]()

- **Poin Penting:** Setelah melakukan `shift()`, baris-baris data di akhir dataset tidak memiliki data label yang valid (karena masa depannya belum ada).

- **Strategi:** Gunakan `df.dropna(inplace=True)` untuk menghapus baris-baris kosong tersebut agar tidak menyebabkan error pada model saat proses pelatihan.

---

## Hal Penting Lain dari Video:

Selain bagian teknis di atas, ada beberapa poin filosofis dalam machine learning yang ditekankan oleh pengajar:

- **Pentingnya Memilih Label yang Realistis:** Pengajar mengingatkan untuk berpikir: "_Apakah ini mungkin dilakukan di dunia nyata?_". Jangan menggunakan fitur yang datanya belum tersedia pada saat prediksi dilakukan (bias classifier), karena itu akan membuat model terlihat sangat akurat di data latihan tetapi gagal total di dunia nyata.

- **Fleksibilitas Variabel:** Menggunakan variabel seperti `forecast_column` dan `forecast_out` (daripada menulis langsung nama kolom atau angka) sangat disarankan agar kode Anda bersifat reusable (dapat digunakan kembali) untuk proyek lain atau dataset yang berbeda di masa depan.

- **Eksperimentasi:** Jangan ragu untuk mengubah nilai seperti `0.01` (1%) untuk melihat bagaimana perubahan tersebut memengaruhi performa model. Tutorial ini bersifat eksploratif, dan hasil terbaik sering ditemukan dengan mencoba berbagai parameter.

_Video Referensi_: [Regression Features and Labels - Practical Machine Learning Tutorial with Python p.3](https://youtu.be/lN5jesocJjk?si=1aI7K1OqSQmXKKx9)
