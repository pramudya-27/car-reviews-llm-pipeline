# CarReview-LLM-Pipeline: Multi-Task NLP Chatbot Prototype

![Car-ing is sharing](car.jpeg)

Proyek ini merupakan *prototype* pipeline NLP berbasis Large Language Models (LLM) yang dibangun untuk **"Car-ing is sharing"**, perusahaan penjualan dan penyewaan mobil. Sistem ini dirancang untuk memproses ulasan pelanggan secara otomatis dengan berbagai kemampuan NLP terintegrasi menggunakan ekosistem **Hugging Face Transformers** dan **PyTorch**.

---

## Studi Kasus (Business Use Case)

CTO "Car-ing is sharing" membutuhkan solusi berbasis AI untuk menganalisis ulasan pelanggan (*car reviews*) dan mendukung operasional *customer service*. Pipeline AI ini mencakup 4 pilar utama:
1. **Analisis Sentimen:** Mengklasifikasikan kepuasan pelanggan dan mengevaluasi performa model (*Accuracy* & *F1 Score*).
2. **Penerjemahan Bahasa (Bahasa Inggris ke Spanyol):** Menerjemahkan ulasan pelanggan untuk pasar Spanyol dan mengukur kualitas terjemahan (*BLEU Score*).
3. **Extractive Question Answering (QA):** Mengekstrak jawaban spesifik secara langsung dari teks ulasan pelanggan berdasarkan pertanyaan pengguna.
4. **Peringkasan Teks (Summarization):** Meringkas ulasan pelanggan yang panjang menjadi ringkasan berdurasi ringkas (~50 token).

---

## 🛠️ Modul & Model yang Digunakan

* **Sentiment Analysis:** `distilbert-base-uncased-finetuned-sst-2-english`
* **Translation (EN ➡️ ES):** `Helsinki-NLP/opus-mt-en-es`
* **Question Answering:** `deepset/minilm-uncased-squad2`
* **Summarization:** `cnicu/t5-small-booksum` / `sshleifer/distilbart-cnn-12-6`
* **Evaluation Metrics:** `evaluate` (Accuracy, F1 Score, BLEU)

---

## 📁 Struktur Direktori Proyek

```text
CarReview-LLM-Pipeline/
├── data/
│   ├── car_reviews.csv            # Dataset ulasan mobil & label sentimen
│   └── reference_translations.txt # Acuan terjemahan bahasa Spanyol
├── car.jpeg                       # Gambar ilustrasi header proyek
├── notebook.ipynb                 # Jupyter Notebook berisi seluruh alur kode
└── README.md                      # Dokumentasi proyek
