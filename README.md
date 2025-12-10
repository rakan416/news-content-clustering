# 📰 Indonesian News Content Clustering

![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20%7C%20Gensim%20%7C%20Pandas-orange)
![Method](https://img.shields.io/badge/Method-Word2Vec%20vs%20TF--IDF-green)

> **Uncovering hidden patterns in Indonesian news using Natural Language Processing.**

## 📌 Tentang Project
Project ini adalah implementasi *Unsupervised Machine Learning* untuk mengelompokkan (clustering) artikel berita bahasa Indonesia secara otomatis berdasarkan **isi konten (body text)**.

Fokus utama eksperimen ini adalah membandingkan dua metode ekstraksi fitur:
1.  **TF-IDF (Term Frequency-Inverse Document Frequency):** Pendekatan statistik klasik.
2.  **Word2Vec ([Pretrained Wikipedia Bahasa Indonesia](https://github.com/deryrahman/word2vec-bahasa-indonesia)):** Pendekatan semantik berbasis *embedding*.

Hasilnya menunjukkan bahwa pendekatan semantik (Word2Vec) mampu menangkap konteks topik jauh lebih baik dibandingkan pendekatan leksikal (TF-IDF), memisahkan topik spesifik seperti "Wabah PMK", "Kriminalitas", hingga "Gadget" dengan akurasi yang lebih tinggi.

## 🎓 Latar Belakang
Project ini dikerjakan sebagai tugas akhir untuk mata kuliah **Text Processing (Semester 3)**.

Tujuan utamanya adalah memahami fundamental pemrosesan teks, mulai dari:
* **Data Acquisition:** Scrapping data berita riil dari portal *Tribunnews*.
* **Preprocessing:** Cleaning, stemming, stopword removal.
* **Feature Extraction:** Membandingkan efektivitas vektor kata.
* **Evaluation:** Menggunakan *Silhouette Score* untuk mengukur kualitas cluster.

### 📊 Key Findings (The Showdown)
Perbandingan kualitas cluster berdasarkan *Silhouette Score*:

| Metode | Silhouette Score | Interpretasi |
| :--- | :--- | :--- |
| **TF-IDF** | `0.030` | **High Noise:** Banyak berita tercampur |
| **Word2Vec (Wiki-ID)** | `0.157` | **Structured:** Peningkatan **5x lipat**! Cluster terbentuk berdasarkan konteks makna, bukan sekadar kata kunci. |

## 🚀 Potensi Implementasi
Hasil dari model clustering ini dapat dikembangkan lebih lanjut untuk berbagai kebutuhan industri:

1.  **News Aggregator App:** Secara otomatis mengelompokkan ratusan berita dari berbagai sumber ke dalam satu topik yang sama (seperti fitur "Full Coverage" di Google News).
2.  **Content Recommendation System:** Merekomendasikan artikel berita lanjutan yang memiliki vektor topik (isi) serupa kepada pembaca.
3.  **Trend Monitoring (Social Listening):** Membantu instansi pemerintah atau PR perusahaan memetakan isu apa yang sedang mendominasi media massa secara *real-time* (misal: Deteksi dini penyebaran isu wabah).

## 🛠️ How to Run
Pastikan Anda memiliki Python yang terinstall di komputer Anda dan ipykernel untuk running jupyter notebook-nya.

1.  **Clone Repository**
    ```bash
    git clone https://github.com/rakan416/news-content-clustering.git
    cd news-content-clustering
    ```

2.  **Install Dependencies**
    ```bash
    pip install pandas numpy scikit-learn gensim nltk matplotlib seaborn
    ```
    *(Pastikan Anda juga mendownload model Word2Vec pretrained dari github [Dery Rahman](https://github.com/deryrahman/word2vec-bahasa-indonesia) model dengan panjang vector 100)*

3.  **Run the Notebook**
    Buka file Jupyter Notebook utama:
    ```bash
    jupyter notebook Text_Processing.ipynb
    ```

## 💡 Quote of the Project
> *"Data is just like crude oil. It’s valuable, but if unrefined it cannot really be used."*
>
> — **Clive Humby**

## 👨‍💻 Authors (Tim Mahasiswa)
Dibuat dengan ☕ dan 💻 oleh:

* **Rakan R. Dewangga**
* **Kristian Bintang**
* **Nachla Fadilla**
