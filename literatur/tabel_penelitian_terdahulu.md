# Studi Literatur — Tabel Penelitian Terdahulu (State of the Art)

Tema penelitian: klasifikasi status pelanggan (langganan/churn) dan klasifikasi perilaku pelanggan menggunakan algoritma Random Forest.
File PDF artikel tersimpan di folder ini (`01_...` s.d. `10_...`).
Sumber pencarian: Google Scholar, Garuda, portal jurnal SINTA; rentang 2022–2026.
**Peringatan:** ranking SINTA tiap jurnal WAJIB diverifikasi ulang di sinta.kemdikbud.go.id sebelum dikutip.

## Tabel Penelitian Terdahulu

| No | Peneliti (Tahun) | Judul & Jurnal | Dataset | Algoritma | Metrik | Hasil | Celah Penelitian |
|---|---|---|---|---|---|---|---|
| 1 | Sidiq & Anggraini (2023) | Analysis and Classification of Customer Churn Using Machine Learning Models. *Jurnal RESTI* 7(6), 1253–1259. **SINTA 2** | Telco Customer Churn (Kaggle) | LR, RF, SVM, Gradient Boosting, AdaBoost, XGBoost; SMOTE | Accuracy, PFI | XGBoost terbaik (akurasi 0,829); SMOTE justru menurunkan akurasi; fitur terpenting: tenure, contract, TV streaming | Belum menguji dataset retail/e-commerce (shopping trends) |
| 2 | Prayogi, Sucipto & Nugroho (2026) | Analisis Prediksi Customer Churn Nasabah Bank dengan Algoritma Random Forest. *Jurnal Teknik Elektro Unisla* | Bank Customer Churn (Kaggle, 10.000 baris) | Random Forest + feature selection | Accuracy, Precision, Recall, F1 | Akurasi 86,7% (tanpa seleksi fitur); seleksi fitur menurunkan sedikit performa | Objek perbankan, bukan pelanggan ritel |
| 3 | Dharma dkk. (2023) | Implementation of Random Forest Algorithm on Sales Data to Predict Potential Churn of Products. *Sinkron* 8(2), 866 | Data penjualan Supermarket Suzuya | RF vs Logistic Regression vs SVM | Accuracy | RF paling efektif: akurasi 96% | Objek churn produk, bukan churn/langganan pelanggan |
| 4 | Muthmainnah & Voutama (2023) | Pendekatan Data Science untuk Menemukan Customer Churn pada Perusahaan Fashion dengan Metode Machine Learning. *Jurnal JSK TGD* 6(2), 463–471 | Data pelanggan fashion/e-commerce | RandomForestClassifier (dari 4 model) | Accuracy | Akurasi 1,00 | Akurasi sempurna sulit direproduksi; tidak ada analisis feature importance |
| 5 | Rodliana (2026) | Penerapan Algoritma Random Forest untuk Klasifikasi Pelanggan Berdasarkan Data Demografi dan Perilaku Belanja. *Skripsi UIN Sunan Ampel Surabaya* | Customer Personality Analysis (Kaggle) | RF + SMOTENC | Accuracy, Precision, Recall, F1 | Akurasi 0,863; F1 0,574 | Menangani kelas tidak seimbang, objek respons promosi, bukan subscription status |
| 6 | Dinata, Abdurrahman & Fitriyah (2023) | Perbandingan Optimasi Algoritma Random Forest Menggunakan Teknik Boosting terhadap Kasus Klasifikasi Churn Pelanggan di Industri Telekomunikasi. *Jurnal JASIE* | Telco churn | RF + XGBoost/AdaBoost | Accuracy, Precision, Recall, F1 | RF+AdaBoost paling optimal: akurasi 0,9913, F1 0,9915 | Fokus telekomunikasi; nilai sangat tinggi perlu diverifikasi ulang |
| 7 | Raharjo, Asmarajati & Ihsannuddin (2025) | Implementasi Metode Random Forest Berbasis Webservices API PPoE untuk Klasifikasi Pelanggan Internet Dial Up. *Jurnal Biner* 4(1), 19 | Data pelanggan ISP CV. Tabung Creative Digital | RF (entropy, gain) | Uji sistem, blackbox | RF berhasil mengklasifikasi dan diimplementasikan sebagai layanan web | Tidak melaporkan metrik akurasi/F1 secara formal |
| 8 | Amaliah, Nusrang & Aswi (2022) | Penerapan Metode Random Forest untuk Klasifikasi Varian Minuman Kopi di Kedai Kopi Konijiwa Bantaeng. *VARIANSI* 4(2), 121–127 | Data penjualan kedai kopi | RF (mtry=2, ntree=500) | Confusion matrix | Akurasi 94,12% | Objek varian produk, bukan pelanggan |
| 9 | Firdaus, Habibie & Rizki (2024) | Implementasi Algoritma Random Forest untuk Klasifikasi Pencemaran Udara di Wilayah Jakarta Berdasarkan Jakarta Open Data. *Jurnal FASILKOM* 14(2), 520–525 | Jakarta Open Data | RF | Precision, Recall, F1, AUC | Akurasi data uji 99,95%; AUC 99,96% | Objek pencemaran udara; domain berbeda |
| 10 | Purnama dkk. (2024) | Perbandingan Performa Algoritma Random Forest dan Gradient Boosting dalam Mengklasifikasi Churn Telco. *Techno.COM* 23(3), 645–657 | Telco churn | RF vs Gradient Boosting | Accuracy, ROC-AUC | Gradient Boosting unggul: akurasi 83%, AUC 0,89 (RF: 81%, AUC 0,87) | Belum menggunakan dataset shopping trends |

## Celah Penelitian (Research Gap) yang Didapat
1. **Sebagian besar penelitian memakai dataset telekomunikasi/perbankan** — belum ada yang memakai dataset **Shopping Trends** untuk klasifikasi status langganan → peluang penelitian ini.
2. Beberapa studi belum melaporkan **feature importance** secara mendalam → penelitian ini mengisi celah lewat pertanyaan penelitian ke-2.
3. Hasil sangat tinggi (akurasi 99%+) pada beberapa studi sulit direproduksi → penelitian ini menggunakan **train-test split dan metrik evaluasi lengkap** (akurasi, precision, recall, F1, confusion matrix).

## Cara Sitasi (format IEEE-style sementara)
```
[1] M. M. Sidiq and D. Anggraini, "Analysis and Classification of Customer Churn Using Machine Learning Models," Jurnal RESTI, vol. 7, no. 6, pp. 1253-1259, 2023.
[2] A. P. A. Prayogi, S. Sucipto, and A. Nugroho, "Analisis Prediksi Customer Churn Nasabah Bank dengan Algoritma Random Forest," Jurnal Teknik Elektro, 2026.
[3] A. Dharma et al., "Implementation of Random Forest Algorithm on Sales Data to Predict Potential Churn of Products," Sinkron, vol. 8, no. 2, p. 866, 2023.
[4] T. N. Muthmainnah and A. Voutama, "Pendekatan Data Science untuk Menemukan Customer Churn pada Perusahaan Fashion dengan Metode Machine Learning," Jurnal JSK TGD, vol. 6, no. 2, pp. 463-471, 2023.
[5] M. A. Rodliana, "Penerapan Algoritma Random Forest untuk Klasifikasi Pelanggan Berdasarkan Data Demografi dan Perilaku Belanja," Skripsi, UIN Sunan Ampel Surabaya, 2026.
[6] N. A. S. Dinata, G. Abdurrahman, and N. Q. Fitriyah, "Perbandingan Optimasi Algoritma Random Forest Menggunakan Teknik Boosting terhadap Kasus Klasifikasi Churn Pelanggan di Industri Telekomunikasi," Jurnal JASIE, 2023.
[7] F. A. Raharjo, D. Asmarajati, and I. A. Ihsannuddin, "Implementasi Metode Random Forest Berbasis Webservices API PPoE untuk Klasifikasi Pelanggan Internet Dial Up," Jurnal Biner, vol. 4, no. 1, p. 19, 2025.
[8] S. Amaliah, M. Nusrang, and A. Aswi, "Penerapan Metode Random Forest untuk Klasifikasi Varian Minuman Kopi di Kedai Kopi Konijiwa Bantaeng," VARIANSI, vol. 4, no. 2, pp. 121-127, 2022.
[9] R. Firdaus, H. Habibie, and Y. Rizki, "Implementasi Algoritma Random Forest untuk Klasifikasi Pencemaran Udara di Wilayah Jakarta Berdasarkan Jakarta Open Data," Jurnal FASILKOM, vol. 14, no. 2, pp. 520-525, 2024.
[10] M. A. Purnama et al., "Perbandingan Performa Algoritma Random Forest dan Gradient Boosting dalam Mengklasifikasi Churn Telco," Techno.COM, vol. 23, no. 3, pp. 645-657, 2024.
```
