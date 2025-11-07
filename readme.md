# Analisis Sentimen Aplikasi BCA Mobile

Project ini bertujuan untuk melakukan analisis sentimen terhadap ulasan pengguna aplikasi BCA Mobile yang diambil dari Google Play Store. Analisis ini menggunakan teknik *Natural Language Processing* (NLP) dan *machine learning* untuk mengklasifikasikan ulasan ke dalam sentimen (misalnya, positif, negatif, atau netral).

---

## Fitur Utama

* **Scraping Data:** Mengambil data ulasan aplikasi BCA Mobile secara otomatis dari Google Play Store.
* **Preprocessing Teks:** Membersihkan dan mempersiapkan data teks ulasan, termasuk *case folding*, *tokenizing*, *stopword removal*, dan *stemming* (menggunakan library Sastrawi).
* **Visualisasi Data:** Membuat visualisasi seperti *word cloud* untuk memahami kata-kata yang paling sering muncul dalam ulasan.
* **Pemodelan Sentimen:** Membangun dan melatih model *machine learning* (seperti XGBoost) untuk memprediksi sentimen dari sebuah ulasan.
* **Evaluasi Model:** Mengevaluasi performa model menggunakan berbagai metrik klasifikasi.

---

## Teknologi yang Digunakan

Proyek ini dibuat dengan Python dan menggunakan *library* berikut (berdasarkan `requirements.txt`):

* **Data Scraper:** `google-play-scraper`
* **Analisis & Manipulasi Data:** `pandas`, `numpy`
* **NLP:** `nltk`, `Sastrawi`
* **Visualisasi Data:** `matplotlib`, `seaborn`, `wordcloud`
* **Machine Learning:** `scikit-learn`, `xgboost`, `imbalanced-learn`
* **Lain-lain:** `gensim`, `Requests`, `protobuf`
* **Environment:** `Jupyter Notebook`

---

## Prasyarat Instalasi

Pastikan Anda memiliki Python 3.x terinstal di sistem Anda.

1.  **Clone repositori ini:**
    ```bash
    git clone [https://github.com/b1n0r10n/sentiment-analysis-bca-mobile.git](https://github.com/b1n0r10n/sentiment-analysis-bca-mobile.git)
    cd sentiment-analysis-bca-mobile
    ```

2.  **Buat dan aktifkan *virtual environment* (dianjurkan):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # Untuk Windows gunakan `venv\Scripts\activate`
    ```

3.  **Instal semua *dependency* yang diperlukan:**
    File `requirements.txt` berisi semua *library* yang dibutuhkan.
    ```bash
    pip install -r requirements.txt
    ```

---

## Dataset

Dataset utama (`ulasanbcamobile2.csv`) berisi kumpulan ulasan pengguna yang diperoleh dari Google Play Store dan sumber publik lain.  
Karena ukuran file melebihi batas GitHub (100 MB), data disimpan terpisah di **GitHub Releases** dan dapat diunduh secara manual atau otomatis.

- **Nama berkas:** `ulasanbcamobile2.csv`  
- **Versi rilis:** `v0.1.0`  
- **Tautan unduh langsung:** [⬇️ Download CSV](https://github.com/b1n0r10n/sentiment-analysis-bca-mobile/releases/download/v0.1.0/ulasanbcamobile2.csv)

### Unduh via Command Line
'''bash
# Buat folder data jika belum ada
mkdir -p data

# Unduh dataset ke dalam folder data
curl -L -o data/ulasanbcamobile2.csv "[https://github.com/b1n0r10n/sentiment-analysis-bca-mobile/releases/download/v0.1.0/ulasanbcamobile2.csv](https://github.com/b1n0r10n/sentiment-analysis-bca-mobile/releases/download/v0.1.0/ulasanbcamobile2.csv)"

---

## Contoh Penggunaan

Untuk menjalankan project ini, Anda dapat membuka dan menjalankan *Jupyter Notebook* yang tersedia di dalam folder `notebooks/`.

1.  **Unduh Dataset:**
    Pastikan Anda telah mengunduh dataset `ulasanbcamobile2.csv` (menggunakan tautan atau *command line* di atas) dan meletakkannya di folder yang sesuai (misalnya, `data/`).

2.  **Jalankan `Data-Scraping.ipynb`:**
    Buka notebook ini untuk mengambil data ulasan terbaru dari Google Play Store (opsional jika Anda hanya ingin menggunakan dataset yang ada).

3.  **Jalankan `Sentiment-Analysis.ipynb`:**
    Setelah data tersedia, buka notebook ini. Notebook ini akan memuat data, melakukan seluruh proses preprocessing, melatih model, dan mengevaluasi hasilnya. Anda dapat melihat dan menjalankan setiap sel kode untuk memahami alur analisis.

---
