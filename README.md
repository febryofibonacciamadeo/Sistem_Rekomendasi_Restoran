# Sistem Rekomendasi Restoran

Sistem rekomendasi restoran yang menyarankan tempat makan kepada pengguna berdasarkan data rating konsumen terhadap restoran.

## Deskripsi

Proyek ini membangun sebuah **recommender system** untuk merekomendasikan restoran kepada pengguna, menggunakan data rating konsumen (`rating_final.csv`) — dataset ini umumnya berasal dari domain *Restaurant & Consumer Data* yang berisi interaksi rating antara konsumen dan restoran.

## Struktur Repository

```
Sistem_Rekomendasi_Restoran/
├── dataset/            # Data restoran & data pendukung lainnya
├── dataset.zip          # Arsip dataset mentah
├── code.ipynb           # Notebook utama: eksplorasi data, pemodelan, evaluasi
└── rating_final.csv     # Data rating konsumen terhadap restoran
```

## Alur Kerja (Workflow)

1. **Data Loading:** memuat data restoran dan rating konsumen (`rating_final.csv`).
2. **Exploratory Data Analysis (EDA):** eksplorasi distribusi rating dan karakteristik restoran/konsumen.
3. **Data Preprocessing:** membersihkan data dan membentuk matriks user-item.
4. **Model Building:** membangun model rekomendasi, misalnya:
   - *Collaborative Filtering* (berbasis kemiripan konsumen/restoran), dan/atau
   - *Content-Based Filtering* (berbasis fitur/kategori restoran)
5. **Evaluation:** mengukur kualitas rekomendasi (mis. RMSE, precision@k).
6. **Rekomendasi:** menghasilkan daftar top-N restoran untuk konsumen tertentu.

## Library yang Digunakan

- Python
- Jupyter Notebook
- pandas & numpy
- scikit-learn (perhitungan similarity, evaluasi model)

## Cara Menjalankan

1. Clone repository ini:
   ```bash
   git clone https://github.com/febryofibonacciamadeo/Sistem_Rekomendasi_Restoran.git
   cd Sistem_Rekomendasi_Restoran
   ```
2. Install dependensi:
   ```bash
   pip install numpy pandas scikit-learn jupyter
   ```
3. Ekstrak dataset jika diperlukan:
   ```bash
   unzip dataset.zip
   ```
4. Jalankan notebook:
   ```bash
   jupyter notebook code.ipynb
   ```

## Hasil

Notebook menghasilkan daftar rekomendasi restoran beserta evaluasi performa model. Lihat `code.ipynb` untuk detail metrik dan contoh output rekomendasi.
