# sentiment-analysis-ibm-granite
Sistem klasifikasi sentimen dan peringkasan otomatis ulasan produk menggunakan model IBM Granite 3.3 8b melalui Replicate API untuk ekstraksi insight dari data tekstual.

📊 Automated Sentiment Classification and Summarization of Product Reviews using IBM Granite 3.3 8b

📌 Project Overview

Proyek ini mengimplementasikan alur kerja analisis data teks end-to-end untuk mengolah ulasan pelanggan yang tidak terstruktur. Dengan menggunakan model IBM Granite 3.3 8b melalui Replicate API, proyek ini mampu melakukan klasifikasi sentimen secara otomatis dan merangkum poin-poin penting dari ratusan baris teks ulasan dalam hitungan detik.

🎯 Masalah & Target Pengguna

Masalah: Perusahaan seringkali menerima ribuan ulasan pelanggan setiap hari. Melakukan pembacaan dan analisis manual terhadap data tekstual ini sangat memakan waktu, subjektif, dan sulit untuk diubah menjadi kebijakan yang terukur.

Target Pengguna: Tim riset produk, manajer operasional e-commerce, dan analis perilaku konsumen yang membutuhkan insight cepat dari opini publik tanpa harus membaca seluruh ulasan satu per satu.

🛠️ Tech Stack & Model AI

Bahasa Pemrograman: Python

Library Utama: Pandas (Data Manipulation), Replicate (AI Integration).

Model AI: ibm-granite/granite-3.3-8b-instruct (Large Language Model unggulan untuk tugas-tugas instruksi teks).

Dataset: Customer Reviews Dataset (Hu & Liu, 2004) - Fokus pada ulasan produk elektronik (Canon G3).

📊 Metodologi Analisis

Proyek ini menggunakan empat langkah utama dalam proses analisisnya:

Data Preprocessing: Mengekstraksi teks mentah dari dataset format .txt legendaris (Hu & Liu) dan mengubahnya menjadi struktur tabel (DataFrame) agar mudah diolah secara batch.

AI Classification (Inference): Mengirimkan data ulasan ke model IBM Granite dengan teknik Zero-Shot Prompting untuk menentukan label sentimen (Positif/Negatif) secara otomatis.

Data Aggregation: Mengelompokkan hasil klasifikasi untuk melihat distribusi persepsi pelanggan terhadap produk.

AI Summarization: Menggunakan kemampuan generatif LLM untuk merangkum seluruh ulasan menjadi poin-poin keunggulan dan kelemahan produk yang ringkas.

💡 Key Insights

Berdasarkan analisis terhadap ulasan kamera Canon G3 menggunakan bantuan AI:

Sentimen Dominan: Mayoritas pengguna memberikan respon sangat positif terhadap kualitas gambar (picture quality) dan kemudahan penggunaan (ease of use).

Keluhan Spesifik: AI berhasil mendeteksi masalah teknis pada bagian viewfinder yang terhalang oleh lensa pada pengaturan tertentu.

Efisiensi: Penggunaan AI menghemat waktu operasional riset hingga lebih dari 90% dibandingkan pelabelan manual, dengan tingkat konsistensi logika yang stabil.

🚀 Actionable Recommendations

Berdasarkan insight di atas, rekomendasi yang diajukan adalah:

Iterasi Desain Produk: Tim pengembangan produk harus meninjau kembali penempatan viewfinder pada model berikutnya agar tidak terhalang oleh lensa fisik saat pengambilan gambar sudut lebar.

Strategi Marketing: Tonjolkan fitur "kemudahan penggunaan" dan "kualitas gambar SLR dalam bentuk point-and-shoot" sebagai nilai jual utama dalam iklan, karena inilah aspek yang paling dicintai oleh pengguna asli.

Mengapa berdampak? Rekomendasi ini bersifat actionable karena didasarkan langsung pada keluhan teknis dan pujian spesifik yang diekstrak oleh AI dari ribuan kata pelanggan.

🧠 Reflection & AI Insight

Pengerjaan proyek ini membuktikan bahwa integrasi LLM seperti IBM Granite ke dalam alur kerja analisis data dapat mengubah data teks yang berantakan menjadi data terstruktur yang siap pakai.

Teknik Prompting Efektif: Teknik Constraint-based Prompting (misal: "Jawab hanya dengan 1 kata") adalah yang paling efisien dalam riset ini. Hal tersebut memastikan output dari AI konsisten dan dapat langsung diintegrasikan kembali ke dalam Pandas DataFrame tanpa perlu proses pembersihan (data cleaning) tambahan di akhir.
