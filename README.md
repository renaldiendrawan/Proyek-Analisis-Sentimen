# Sentiment Analysis of Google Play Store Reviews 🇮🇩

Proyek ini bertujuan untuk melakukan analisis sentimen terhadap ulasan pengguna dari aplikasi Android yang diambil langsung dari Google Play Store. Analisis ini menggunakan pendekatan machine learning dan lexicon-based labeling untuk mengkategorikan ulasan menjadi **positif**, **netral**, dan **negatif**.

---

## 🔧 Struktur Proyek

```

.
├── scraper.ipynb               # Notebook untuk scraping review dari Google Play Store
├── sentiment\_analysis.ipynb    # Notebook utama untuk preprocessing, pelabelan, training, evaluasi, dan inference model
├── dataset/
│   └── dataset_ulasan_com_dafturn_mypertamina  # Dataset hasil scraping
├── output/
│   └── Word Cloud dan Bar Chart
├── requirements.txt            # Daftar dependensi proyek beserta versinya
└── README.md                   # Dokumentasi ini

````

---

## 🧪 Tools & Library yang Digunakan

- `google-play-scraper`: Mengambil data ulasan aplikasi dari Google Play Store
- `pandas`, `numpy`: Manipulasi dan analisis data
- `nltk`, `textblob`, `gensim`: Preprocessing teks dan lexicon-based sentiment
- `scikit-learn`, `imbalanced-learn`: Model machine learning & teknik balancing data (SMOTE)
- `tensorflow`: Untuk kemungkinan ekstensi ke model berbasis deep learning
- `matplotlib`, `seaborn`, `wordcloud`: Visualisasi data

---

## 📦 Instalasi

```bash
pip install -r requirements.txt
````

Jika menggunakan Google Colab, cukup unggah file notebook dan jalankan setiap cell secara berurutan.

---

## 🚀 Langkah Penggunaan

1. Jalankan `scraper.ipynb` untuk mengambil data ulasan dari Google Play.

   * Pastikan mengganti `package name` aplikasi yang sesuai.
   * Simpan hasil scraping ke dalam file `CSV`.

2. Jalankan `sentiment_analysis.ipynb` untuk:

   * Preprocessing teks
   * Visualisasi Word Cloud
   * Pelabelan sentimen secara otomatis
   * Pembagian data training dan testing (2 skema: 80:20 dan 70:30)
   * Pelatihan model (SVM, Random Forest, XGBoost)
   * Evaluasi akurasi pada **training dan testing set**
   * Testing/inference input teks manual menggunakan fungsi khusus

---

## 📊 Model dan Skema Pelatihan

Model yang digunakan:

* Support Vector Machine (SVM)
* Random Forest
* XGBoost

Setiap model diuji dalam skema pembagian data:

* 80% training : 20% testing
* 70% training : 30% testing

Akurasi minimal yang dicapai: **> 92%** pada training dan testing set.

---

## 🤖 Inference (Uji Model)

Notebook dilengkapi fungsi `predict_sentiment(text)` untuk menguji teks ulasan baru dan memprediksi kelas sentimennya. Kategori output:

* **Positif**
* **Netral**
* **Negatif**

Contoh:

```python
predict_sentiment("Aplikasinya sangat membantu dan mudah digunakan.")
# Output: "Positif"
```

---

## 📈 Visualisasi dan Analisis

* Word Cloud: Untuk melihat kata yang sering muncul
* Distribusi Label: Bar chart dari jumlah sentimen

---

## 📌 Catatan Tambahan

* Dataset hasil scraping minimal 10.000 baris
* Dilakukan balancing data menggunakan SMOTE
* Lexicon-based labeling dilakukan berdasarkan asumsi rating atau frasa positif/negatif
* Siap diperluas menggunakan model BERT, GloVe, atau FastText

---

## ✍️ Kontributor

* 📛 Nama: \Renaldi Endrawan
* 📧 Email: \renaldiendrawan@gmail.com
* 🚀 Dicoding Submission: Machine Learning Developer - Text Classification

---

## ⚖️ Lisensi

Proyek ini bersifat open-source dan digunakan untuk keperluan edukasi dan evaluasi. Silakan gunakan, modifikasi, dan distribusikan sesuai kebutuhan dengan tetap menyertakan atribusi yang sesuai.
