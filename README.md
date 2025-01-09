# **Evaluasi Model Q&A**

Repository ini berisi kode dan dokumentasi untuk mengevaluasi model Q&A yang bertujuan untuk mengekstraksi dan mencari informasi dari putusan pengadilan terkait kasus pidana khusus narkotika PN Rantau Prapat 2024. Model ini mengintegrasikan teknik seperti web scraping, pembuatan embedding, dan sistem Q&A berbasis AI menggunakan Groq AI.

---

## **Pendahuluan**

Project ini bertujuan untuk membangun dan mengevaluasi model Q&A yang dapat membantu dalam mencari dan menganalisis informasi dari putusan pengadilan. Tahapan utama dalam proyek ini meliputi:
- Scraping data putusan pengadilan.
- Membuat dataset Q&A berbasis konteks.
- Meningkatkan kemampuan pencarian menggunakan embedding.
- Memanfaatkan Groq AI untuk pemahaman bahasa yang lebih baik.

---

## **Fitur**

- **Scraping Data:** Mengambil data putusan pengadilan dari situs resmi.
- **Pembentukan Dataset Q&A:** Menggunakan API Groq untuk membuat pertanyaan dan jawaban berbasis konteks hukum.
- **Embedding:** Mengubah teks menjadi representasi vektor untuk meningkatkan akurasi pencarian.
- **Pencarian Berbasis Embedding:** Menggunakan model kesamaan kosinus untuk mendapatkan jawaban paling relevan.
