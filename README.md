# Skripsi — Riset Berbasis Data

## Deskripsi Proyek
Penelitian ini membahas prediksi status langganan pelanggan (`Subscription Status`) pada dataset perilaku belanja pelanggan (`shopping_trends.csv`) menggunakan teknik data mining / machine learning klasifikasi.

**Topik:** Klasifikasi perilaku pelanggan e-commerce menggunakan machine learning

**Judul Penelitian:**
Klasifikasi Status Langganan pada Dataset Shopping Trends Menggunakan Algoritma Random Forest

**Unsur Judul:**
- Jenis penelitian: Klasifikasi (machine learning)
- Objek/variabel penelitian: Status Langganan Pelanggan (`Subscription Status`)
- Subjek penelitian: Pelanggan pada dataset perilaku belanja
- Metode/algoritma: Random Forest
- Lokasi: Dataset Shopping Trends (Kaggle)

**Pertanyaan Penelitian:**
1. Bagaimana performa algoritma Random Forest dalam memprediksi `Subscription Status` pelanggan?
   → Diukur dengan akurasi, precision, recall, F1-score, dan confusion matrix.
2. Fitur apa saja yang paling berpengaruh terhadap status langganan pelanggan?
   → Dijawab dengan analisis feature importance dari model Random Forest.

**Pendekatan:**
1. Pemahaman data (EDA) terhadap `data/raw/shopping_trends.csv`
2. Persiapan data: encoding fitur kategorikal, normalisasi, pembagian train/test → `data/processed/`
3. Pemodelan klasifikasi dengan Random Forest di `notebook/`
4. Evaluasi model: akurasi, precision, recall, F1-score, confusion matrix
5. Penyimpanan model terbaik ke `model/` dan penulisan hasil di `draft/`

## Struktur Folder
- `literatur/` — PDF jurnal, catatan tinjauan pustaka
- `data/raw/` — data mentah (TIDAK PERNAH diubah)
- `data/processed/` — data hasil cleaning dan transformasi
- `notebook/` — Jupyter Notebook: EDA, eksperimen
- `model/` — model tersimpan (.pkl), log eksperimen
- `draft/` — draf proposal, skripsi, artikel

## Sumber Data
- Dataset: `shopping_trends.csv` (3900 baris x 19 kolom, disimpan di `data/raw/`)
- Kolom utama: Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount (USD), Location, Size, Color, Season, Review Rating, Subscription Status, Payment Method, Shipping Type, Discount Applied, Promo Code Used, Previous Purchases, Preferred Payment Method, Frequency of Purchases
- Catat sumber, tanggal unduh, dan lisensi di sini.

## Studi Literatur (State of the Art)
Tabel penelitian terdahulu lengkap tersimpan di `literatur/tabel_penelitian_terdahulu.md` (10 artikel, PDF tersedia di folder `literatur/`). Ringkasannya:

| No | Peneliti (Tahun) | Dataset | Algoritma | Hasil | Celah |
|---|---|---|---|---|---|
| 1 | Sidiq & Anggraini (2023), Jurnal RESTI (SINTA 2) | Telco Churn (Kaggle) | LR, RF, SVM, GB, AdaBoost, XGBoost | XGBoost terbaik, akurasi 0,829 | Belum pakai dataset retail |
| 2 | Prayogi dkk. (2026), Jurnal Teknik Elektro Unisla | Bank Churn (10.000 baris) | Random Forest + feature selection | Akurasi 86,7% | Objek perbankan |
| 3 | Dharma dkk. (2023), Sinkron | Penjualan Supermarket Suzuya | RF vs LR vs SVM | RF akurasi 96% | Objek churn produk |
| 4 | Muthmainnah & Voutama (2023), Jurnal JSK TGD | Pelanggan fashion/e-commerce | RandomForestClassifier | Akurasi 1,00 | Tanpa feature importance |
| 5 | Rodliana (2026), Skripsi UINSA | Customer Personality Analysis | RF + SMOTENC | Akurasi 0,863; F1 0,574 | Objek respons promosi |
| 6 | Dinata dkk. (2023), Jurnal JASIE | Telco churn | RF + XGBoost/AdaBoost | RF+AdaBoost: akurasi 0,9913 | Fokus telekomunikasi |
| 7 | Raharjo dkk. (2025), Jurnal Biner | Pelanggan ISP | RF (entropy, gain) | Uji sistem blackbox | Tanpa metrik formal |
| 8 | Amaliah dkk. (2022), VARIANSI | Penjualan kedai kopi | RF (mtry=2, ntree=500) | Akurasi 94,12% | Objek varian produk |
| 9 | Firdaus dkk. (2024), Jurnal FASILKOM | Jakarta Open Data | RF | Akurasi uji 99,95%; AUC 99,96% | Domain berbeda |
| 10 | Purnama dkk. (2024), Techno.COM | Telco churn | RF vs Gradient Boosting | GB: akurasi 83%, AUC 0,89 | Belum pakai shopping trends |

**Research gap yang diangkat:** belum ada penelitian klasifikasi `Subscription Status` pada dataset Shopping Trends (Kaggle) dengan algoritma Random Forest yang disertai analisis feature importance.
**Catatan:** ranking SINTA tiap jurnal masih WAJIB diverifikasi di sinta.kemdikbud.go.id.

## Cara Menjalankan
1. (opsional) Buat environment: `conda create -n skripsi python=3.10`
2. Pasang pustaka: pandas, numpy, matplotlib, seaborn, scikit-learn
3. Buka notebook dengan Jupyter atau Google Colab, mulai dari notebook bernomor 01.

## Catatan
- Jangan mengubah berkas di `data/raw/`.
- Semua data olahan dihasilkan oleh kode di `notebook/`.
