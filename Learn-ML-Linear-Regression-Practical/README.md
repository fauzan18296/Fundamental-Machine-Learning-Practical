# 📈 Stock Price Prediction: Linear Regression

Proyek ini adalah implementasi praktis dari Machine Learning menggunakan algoritma **Linear Regression** untuk memproses dan memprediksi tren harga saham. Proyek ini merupakan bagian dari rangkaian tutorial pembelajaran mandiri untuk memahami alur kerja data sains dari awal.

---

# 🚀 Deskripsi Proyek

Tujuan utama dari proyek ini adalah melakukan Feature Engineering pada data historis harga saham (Wiki Prices). Alih-alih menggunakan data harga mentah secara langsung, kita mengolah data tersebut untuk menghasilkan fitur yang lebih informatif bagi model, seperti:

- **Volatilitas Harian (HL_PCT):** Selisih antara harga tertinggi dan terendah.

- **Momentum Harian (PCT_change):** Persentase perubahan harga dari pembukaan hingga penutupan.

---

# 🧠 Catatan Reflektif

"Apakah `adj_close` akan menjadi fitur atau target label kita?"

Berdasarkan alur tutorial yang diikuti, hipotesis utama kita adalah kolom `adj_close` akan bertindak sebagai **Target Label** yang ingin diprediksi nilainya di masa depan, sementara fitur lainnya akan menjadi atribut pendukung dalam proses pelatihan model.

---

# 🛠 Teknologi & Library

Proyek ini menggunakan beberapa pustaka Python utama:

- **pandas:** Untuk manipulasi dan analisis data.

- **kagglehub:** Untuk integrasi data langsung dari platform Kaggle (tanpa mengunduh file besar ke dalam repositori).

- **scikit-learn:** Untuk implementasi algoritma regresi.

# 📋 Cara Menjalankan

### 1. Clone repositori ini:

```bash
git clone https://github.com/fauzan18296/Fundamental-Machine-Learning-Practical.git
```

### 2. Instal dependensi dan Set up environment:

**2.1** Setup Virtual Environment
Set up virtual environtment berguna untuk menghindari konflik dependensi sistem local.

- di Linux
  1. buat folder `.venv`
  2. Setup virtual environtment dan Aktifkan virtual environment.

```bash
$ python -m pip venv .venv
$ source .venv/bin/activate
```

- di Windows
  1. buat folder `.venv`
  2. Setup virtual environtment dan Aktifkan virtual environment.

di CMD:

```cmd
C:\> python -m pip venv .venv
C:\> .venv\Scripts\activate.bat
```

di Powershell:

```powershell
PS C:\> python -m pip venv .venv
PS C:\> .venv\Scripts\Activate.ps1
```

**2.2** Instal dependensi

**1. Clone repositori ini:**

```bash
$ git clone https://github.com/fauzan18296/Fundamental-Machine-Learning-Practical.git
```

**3. Instal dependensi:**

```bash
$ python -m pip install -r requirements.txt
```

**3. Jalankan script:**

```bash
$ python main.py
```

> (**Catatan:** Pastikan Anda memiliki koneksi internet, karena `kagglehub` akan mengunduh dataset secara otomatis saat pertama kali dijalankan).
