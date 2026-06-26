# Proyek: Prediksi Regresi Harga Saham (Machine Learning)

Dokumentasi ini mencakup langkah-langkah dalam menyiapkan fitur dan label untuk model regresi harga saham menggunakan Python, Pandas, dan Scikit-Learn

## 📋 Daftar Isi

1. Deskripsi Proyek

2. Prasyarat

3. Penjelasan Kode

4. Konsep Utama

5. Referensi

---

## 🚀 Deskripsi Proyek

Proyek ini bertujuan untuk membangun model machine learning yang dapat memprediksi harga saham di masa depan. Fokus utama dari modul ini adalah melakukan feature engineering dan menyiapkan label (target prediksi) agar data dapat diproses oleh algoritma regresi.

---

## 🛠 Prasyarat

- Clone repositori ini:

```bash
$ git clone https://github.com/fauzan18296/Fundamental-Machine-Learning-Practical.git
```

- Pastikan Anda telah menginstal pustaka berikut di lingkungan Python Anda:

```bash
$ python -m pip install -r requirements.txt
```

---

## 💻 Penjelasan Kode

Berikut adalah cuplikan kode utama yang digunakan untuk menyiapkan dataset:

```python
import math

# 1. Menentukan kolom target prediksi
forecast_column = 'adj_close'

# 2. Menangani missing data (mengganti NaN dengan outlier)
df.fillna(-99999, inplace=True)

# 3. Menentukan seberapa jauh ke depan prediksi dilakukan (misal: 1% dari data)
forecast_out = int(math.ceil(0.01 * len(df)))

# 4. Membuat kolom 'label' dengan menggeser data harga ke depan
df['label'] = df[forecast_column].shift(-forecast_out)

# 5. Membersihkan baris data yang kosong setelah pergeseran
df.dropna(inplace=True)
```

## 💡 Konsep Utama

### Mengapa Mengisi Data dengan `-99999`?

Alih-alih menghapus data yang hilang, kita mengisi dengan angka ekstrem agar model menganggapnya sebagai outlier (pencilan). Ini membantu menjaga integritas kolom lain yang mungkin masih memiliki informasi berharga.

## Peran Fungsi `shift()`

Fungsi `.shift(-forecast_out)` adalah jantung dari proyek ini. Ia memindahkan data harga di masa depan ke baris hari ini, sehingga model dapat mempelajari pola: "_Jika fitur-fitur hari ini adalah X, maka harga di masa depan akan menjadi Y._"

---

## 📚 Referensi

- **Tutorial Asli:** [Regression Features and Labels - Practical Machine Learning Tutorial with Python p.3](https://www.google.com/search?q=https://youtu.be/lN5jesocJjk)

- **Dokumentasi:** [Pandas Documentation](https://www.google.com/search?q=https://pandas.pydata.org/docs/)

---

## 📝 Tips untuk Masa Depan

- Jika Anda ingin memprediksi harga untuk jangka waktu yang lebih lama, cukup ubah nilai **0.01** pada variabel `forecast_out`.

- Selalu pastikan untuk melakukan `dropna()` agar tidak ada data kosong yang masuk ke dalam proses pelatihan model.
