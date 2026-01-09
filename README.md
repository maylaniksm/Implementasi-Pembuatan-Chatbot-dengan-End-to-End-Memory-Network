# 🤖 Chatbot Implementation Using End-to-End Memory Network (MemN2N)

<p align="center">
  <b>Implementasi Chatbot Berbasis Konteks Menggunakan End-to-End Memory Network</b><br/>
  <i>Studi Kasus: Facebook bAbI Tasks – Single Supporting Fact</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/NLP-Chatbot-blue" />
  <img src="https://img.shields.io/badge/Model-End--to--End%20Memory%20Network-green" />
  <img src="https://img.shields.io/badge/Dataset-Facebook%20bAbI-orange" />
  <img src="https://img.shields.io/badge/Framework-TensorFlow%20%7C%20Keras-red" />
  <img src="https://img.shields.io/badge/Status-Completed-success" />
</p>

---

## 📌 Deskripsi Proyek

Proyek ini membahas **implementasi pembuatan chatbot berbasis Artificial Intelligence (AI)** menggunakan pendekatan **End-to-End Memory Network (MemN2N)**. Chatbot dirancang untuk mampu memahami **konteks percakapan** dan menjawab pertanyaan berdasarkan informasi yang tersimpan dalam memori.

Pendekatan ini sangat relevan dalam bidang **Natural Language Processing (NLP)** karena memungkinkan sistem dialog untuk tidak hanya memproses input secara individual, tetapi juga mempertimbangkan **informasi dari percakapan sebelumnya**.

---

## 🎓 Informasi Akademik

* **Nama**: Maylani Kusuma Wardhani
* **NIM**: 202210370311123
* **Mata Kuliah**: Pemrosesan Bahasa Alami (NLP)
* **Kelas**: NLP C
* **Dosen Pengampu**: Vinna Rahmayanti S, S.Si., M.Si
* **Institusi**: Universitas Muhammadiyah Malang
* **Tahun**: 2025

---

## 🎯 Tujuan Proyek

Tujuan utama dari proyek ini adalah:

* Mempelajari konsep **End-to-End Memory Network** dalam sistem chatbot
* Mengimplementasikan model chatbot berbasis **deep learning** secara end-to-end
* Melatih model agar mampu menjawab pertanyaan berbasis cerita (*story-based question answering*)
* Menganalisis performa model dalam memahami konteks dialog sederhana

---

## 📂 Dataset

Dataset yang digunakan berasal dari **Facebook bAbI Tasks**, yaitu kumpulan dataset yang dirancang untuk menguji kemampuan pemahaman teks dan penalaran logis pada sistem AI.

### Dataset yang Digunakan:

* **Task 1: Single Supporting Fact**

### Karakteristik Dataset:

* Berupa cerita pendek (beberapa kalimat)
* Satu pertanyaan untuk setiap cerita
* Satu jawaban yang bergantung pada **satu fakta penting** dalam cerita

Dataset ini sangat cocok untuk memahami cara kerja **model berbasis memori** seperti MemN2N.

---

## ⚙️ Tahapan Implementasi

### 1️⃣ Persiapan Data

* Dataset diunduh secara otomatis menggunakan skrip Python
* Data dibagi menjadi:

  * Data latih (*training set*)
  * Data uji (*testing set*)
* Parsing dilakukan untuk memisahkan:

  * Story
  * Question
  * Answer

---

### 2️⃣ Tokenisasi dan Vektorisasi

* Seluruh teks diubah menjadi token (kata)
* Dibangun **dictionary (word2idx)** untuk mengonversi kata ke indeks numerik
* Dilakukan **padding** agar panjang cerita dan pertanyaan seragam

Tahap ini penting agar data dapat diproses oleh neural network.

---

### 3️⃣ Arsitektur Model End-to-End Memory Network

Model dibangun menggunakan komponen utama berikut:

* **Embedding Layer**

  * Mengubah kata menjadi vektor numerik
* **Memory Representation**

  * Menyimpan representasi cerita dalam memori
* **Matching Mechanism**

  * Menggunakan operasi *dot product* antara pertanyaan dan memori
* **Softmax Layer**

  * Menentukan jawaban yang paling relevan

### Konfigurasi Model:

* Loss Function: `categorical_crossentropy`
* Optimizer: `RMSprop`
* Metrics: `accuracy`

---

## 🚀 Proses Pelatihan Model

* Model dilatih menggunakan data training
* Proses training dilakukan selama beberapa epoch
* Selama pelatihan, metrik berikut dipantau:

  * Training Accuracy
  * Training Loss

Ukuran dataset yang relatif kecil membuat proses training berlangsung cepat.

---

## 📊 Evaluasi dan Hasil

Hasil evaluasi menunjukkan bahwa:

* Model mencapai **akurasi tinggi** pada data pengujian
* Chatbot mampu:

  * Mengidentifikasi fakta yang relevan
  * Memberikan jawaban yang sesuai dengan konteks cerita
* Model berhasil melakukan generalisasi dengan baik

### Visualisasi:

* Grafik akurasi model
* Grafik perkembangan loss selama pelatihan
* Tabel hasil prediksi chatbot

---

## 🧠 Analisis Model

Keunggulan utama **End-to-End Memory Network** terletak pada kemampuannya untuk:

* Menyimpan informasi dalam memori
* Mengakses kembali informasi tersebut saat menjawab pertanyaan
* Menjaga konteks percakapan sederhana

Hal ini menjadikan MemN2N sangat efektif untuk:

* Chatbot berbasis cerita
* Question Answering
* Sistem dialog sederhana

---

## 📌 Kesimpulan

Berdasarkan hasil implementasi dan evaluasi, dapat disimpulkan bahwa:

* End-to-End Memory Network efektif untuk membangun chatbot berbasis konteks
* Dataset bAbI Tasks sangat membantu dalam memahami konsep NLP berbasis memori
* Teknik tokenisasi, padding, embedding, dan softmax sangat berperan dalam pipeline NLP

Model ini dapat dijadikan dasar untuk pengembangan chatbot yang lebih kompleks.

---

## 🔮 Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan ke depannya:

* Menggunakan **task bAbI lainnya**
* Menambahkan **multi-hop memory**
* Mengembangkan chatbot ke dataset dunia nyata
* Mengintegrasikan dengan antarmuka web atau aplikasi

---

## 🔗 Lampiran

* 📓 **Google Colab**:
  [https://colab.research.google.com/drive/1vUebFu2jQ8SqHAJ4h81Ms2pdy_GH6SOE?usp=sharing](https://colab.research.google.com/drive/1vUebFu2jQ8SqHAJ4h81Ms2pdy_GH6SOE?usp=sharing)

* 🎓 **Sertifikat Course Udemy NLP**:
  [https://drive.google.com/drive/folders/1OwJc_0mhYmZCF4B5DDznWcgAhjWcX6DW?usp=sharing](https://drive.google.com/drive/folders/1OwJc_0mhYmZCF4B5DDznWcgAhjWcX6DW?usp=sharing)

* 📺 **Video Presentasi**:
  [https://youtu.be/vaREqHQSr34?si=aEGeUa5-In9d2Ebr](https://youtu.be/vaREqHQSr34?si=aEGeUa5-In9d2Ebr)

---

✨ *README ini dibuat sebagai dokumentasi akademik dan portofolio proyek Natural Language Processing.*
