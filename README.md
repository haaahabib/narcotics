# Evaluasi Model Q&A untuk Putusan Pengadilan

Repositori ini berisi kode dan dokumentasi untuk membangun dan mengevaluasi model Q&A yang bertujuan mengekstraksi informasi dari putusan pengadilan terkait kasus pidana khusus narkotika PN Rantau Prapat 2024.

---

## Daftar Isi

1. [Pendahuluan](#pendahuluan)
2. [Tujuan Proyek](#tujuan-proyek)
3. [Fitur Utama](#fitur-utama)
4. [Tech Stack](#tech-stack)
5. [Alur Kerja Proyek](#alur-kerja-proyek)
6. [Cara Menggunakan](#cara-menggunakan)

---

## **Pendahuluan**

Proyek ini dirancang untuk mengatasi tantangan dalam mengakses dan menganalisis informasi spesifik dari dokumen hukum yang padat teks, seperti putusan pengadilan. Dengan mengintegrasikan teknik-teknik modern seperti web scraping untuk pengumpulan data, pembuatan embedding untuk pemahaman kontekstual, dan pemanfaatan Large Language Model (LLM) melalui Groq AI, model ini dapat memberikan jawaban yang relevan dan akurat terhadap pertanyaan yang diajukan dalam bahasa alami.

## **Tujuan Proyek**

- **Mengotomatisasi Ekstraksi Informasi:** Secara otomatis mengumpulkan data putusan pengadilan dari sumber publik.
- **Membangun Dataset Kontekstual:** Membuat pasangan pertanyaan dan jawaban (Q&A) yang relevan dari isi dokumen hukum.
- **Meningkatkan Akurasi Pencarian:** Mengimplementasikan pencarian berbasis kesamaan semantik (embedding) untuk menemukan informasi yang paling relevan.
- **Menyediakan Antarmuka Interaktif:** Memanfaatkan kecepatan Groq AI untuk menciptakan sistem Q&A yang responsif dan cerdas bagi pengguna.

---

## **Fitur Utama**

- **Web Scraping:** Modul untuk mengambil data putusan pengadilan secara otomatis dari situs Mahkamah Agung.
- **Pembuatan Dataset Q&A:** Skrip untuk menghasilkan pertanyaan dan jawaban secara otomatis dari teks putusan menggunakan Groq AI.
- **Konversi ke Embedding:** Proses untuk mengubah seluruh teks putusan dan dataset Q&A menjadi representasi vektor numerik.
- **Pencarian Berbasis Embedding:** Sistem pencarian yang menggunakan *Cosine Similarity* untuk mencocokkan pertanyaan pengguna dengan jawaban yang paling relevan di dalam database.
- **Integrasi Groq AI:** Pemanfaatan LLM untuk memahami pertanyaan pengguna dan menghasilkan jawaban yang koheren.

---

## **Tech Stack**

- **Bahasa Pemrograman:** Python
- **Library Utama:**
  - `requests` & `BeautifulSoup` (untuk Web Scraping)
  - `pandas` (untuk manipulasi data)
  - `scikit-learn` (untuk Cosine Similarity)
  - `sentence-transformers` (untuk membuat embedding)
  - `groq` (untuk interaksi dengan LLM)
- **Model AI:** Groq AI, All-MiniLM-L6-v2 (atau model embedding lainnya)

---

## **Alur Kerja Proyek**

1.  **Pengumpulan Data:** Data putusan di-scrape dari direktori putusan pengadilan.
2.  **Pra-pemrosesan Teks:** Teks dari putusan dibersihkan dan disiapkan.
3.  **Pembuatan Dataset Q&A:** Teks bersih dikirim ke Groq AI untuk dibuatkan pasangan pertanyaan dan jawaban.
4.  **Pembuatan Embedding:** Seluruh data teks diubah menjadi vektor embedding.
5.  **Proses Pencarian:**
    - Pengguna memasukkan pertanyaan.
    - Pertanyaan diubah menjadi vektor embedding.
    - Dilakukan pencarian kesamaan kosinus antara embedding pertanyaan dengan embedding data yang ada.
    - Jawaban yang paling relevan ditampilkan kepada pengguna.

---

## **Cara Menggunakan**

1.  **Clone Repository Ini**
    ```bash
    git clone https://github.com/haaahabib/narcotics.git
    ```
2.  **Masuk ke Direktori Proyek**
    ```bash
    cd [Nama Folder]
    ```
3.  **Install Dependensi**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Jalankan Skrip Utama**
    ```bash
    python main.py
    ```

*(Catatan: Pastikan Anda sudah mengatur API Key untuk Groq AI di environment variables Anda.)*
