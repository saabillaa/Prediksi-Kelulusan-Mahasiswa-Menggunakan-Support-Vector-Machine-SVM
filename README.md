Prediksi Kelulusan Mahasiswa Menggunakan Support Vector Machine (SVM)

Project Machine Learning — Supervised Classification

1. Deskripsi Proyek

Proyek ini bertujuan untuk memprediksi status kelulusan mahasiswa (Lulus / Belum Lulus) menggunakan algoritma Support Vector Machine (SVM). Dataset berisi atribut akademik dan aktivitas mahasiswa seperti IPK, jumlah SKS, lama studi, dan fitur lain yang berpengaruh terhadap kelulusan.

Proyek dikerjakan menggunakan Python (Google Colab / Jupyter Notebook) dan mengikuti tahapan Machine Learning mulai dari eksplorasi data hingga evaluasi model.

2. Dataset

Nama file: datakelulusanmahasiswa.csv
Sumber: Google Sheets (sesuai link dari dosen)

Dataset berisi beberapa fitur, contoh:

IPK

Total SKS

Umur

Lama Studi

Kehadiran

Keaktifan Organisasi

Nilai Mata Kuliah

Label: Lulus / Belum Lulus

Pada notebook dilakukan:

Pembacaan dataset dengan pandas

Pengecekan missing values

Eksplorasi data & visualisasi

3. Langkah Pengerjaan Proyek

Tahapan yang dilakukan pada notebook (SVM_2391_SABILLA_3A.ipynb) adalah sebagai berikut:

A. Setup & Load Dataset

Import library: pandas, numpy, sklearn, matplotlib

Load dataset CSV

Menampilkan 5 baris awal

Identifikasi fitur & label

Cek missing values

B. Exploratory Data Analysis (EDA)

Statistik deskriptif (mean, std, min, max)

Visualisasi:

Histogram IPK

Countplot Lulus vs Tidak Lulus

Analisis:

Perbandingan distribusi IPK mahasiswa lulus vs tidak

Fitur yang paling berpengaruh secara visual

C. Preprocessing Data

Penanganan missing values

Encoding data kategorikal (LabelEncoder / OneHotEncoder)

StandardScaler (karena SVM sensitif terhadap skala)

Train–test split:

60:40

75:25

80:20

90:10

D. Training Model SVM

Model yang dibangun:

SVM Linear

SVM RBF

Hyperparameter tuning meliputi:

C = {0.1, 1, 10}

gamma = {scale, 0.1, 1}

kernel = {linear, rbf}

Hasil yang ditampilkan:

Confusion Matrix

Classification Report

Akurasi

Precision, Recall, F1-score

Analisis:

Perbandingan performa Linear vs RBF

Pengaruh parameter C

Apakah dataset bersifat linearly separable

E. Model Interpretation

Pada bagian ini dijelaskan:

Fitur paling berpengaruh terhadap kelulusan

Interpretasi hubungan IPK rendah terhadap status kelulusan

Insight keseluruhan model

F. Deployment Sederhana

Sebuah fungsi dibuat untuk memprediksi status mahasiswa:

predict_status(ipk, sks, umur, lamastudi, ...)


Fungsi memanggil model SVM yang sudah dilatih dan mengeluarkan hasil Lulus / Tidak Lulus.

G. Dokumentasi & Upload GitHub

Repository berisi:

Notebook lengkap: SVM_kelulusan.ipynb

Dataset folder /data/datakelulusanmahasiswa.csv

README.md

Screenshot hasil prediksi model

4. Hasil Evaluasi Model

Ringkasan hasil (sesuaikan dengan output notebook):

Model RBF cenderung memberikan akurasi lebih tinggi daripada Linear

Nilai C yang lebih besar meningkatkan kompleksitas model

Dataset tidak sepenuhnya linearly separable → RBF lebih optimal

Fitur seperti IPK dan Lama Studi memiliki pengaruh besar dalam prediksi

Seluruh grafik, tabel, dan perhitungan lengkap tersedia dalam notebook.

5. Cara Menjalankan Notebook

Clone repository:

git clone https://github.com/USERNAME/NAMA-REPO.git


Buka notebook:

Google Colab atau

Jupyter Notebook lokal

Pastikan library berikut terinstall:

pip install pandas numpy scikit-learn matplotlib seaborn


Jalankan setiap cell dari atas sampai bawah

Uji fungsi prediksi di bagian deployment

6. Identitas Mahasiswa

Nama: Sabilla
NIM: 2391
Kelas: 3A SI
Mata Kuliah: Machine Learning
Dosen Pengampu: Dr. DWI WAHYU PRABOWO, S.Si., M.Eng., Dody Erlangga, S.Kom
