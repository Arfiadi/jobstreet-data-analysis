# JobStreet Data Analysis (Indonesia)

Proyek ini adalah analisis data *end-to-end* yang berfokus pada lowongan pekerjaan yang di-scrape dari JobStreet Indonesia. Proyek ini mencakup pembersihan data (data cleaning), preprocessing, dan Exploratory Data Analysis (EDA) untuk menemukan *insight* tentang pasar kerja saat ini.

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis tren pasar kerja, meliputi:
- *Job titles* dan spesialisasi yang paling banyak dicari.
- Distribusi pekerjaan berdasarkan kota dan provinsi di Indonesia.
- Distribusi dan tren gaji.
- Perusahaan perekrut (*top recruiters*) yang paling aktif membuka lowongan.

## 📂 Struktur Repositori
- `Analisis_data_jobstreet.ipynb`: Jupyter Notebook utama yang berisi proses *preprocessing*, pembersihan data, dan visualisasi (*EDA*).
- `jobstreet_data_jobs_hasilscraping.xlsx`: Dataset mentah hasil *scraping* dari JobStreet sebelum dibersihkan.
- `jobstreet_data_jobs_final.xlsx`: Dataset yang sudah dibersihkan dan siap untuk dianalisis.

## 🛠️ Teknologi yang Digunakan
- **Bahasa**: Python
- **Library**: Pandas, Matplotlib, Seaborn

## 📊 Hasil Analisis Utama
1. **Data Preprocessing**: Menangani *missing values*, menormalisasi teks (*job titles*, spesialisasi), melakukan *parsing* pada rentang gaji menjadi format numerik yang dapat dihitung, serta mengekstrak informasi kota/provinsi dari string lokasi mentah.
2. **Exploratory Data Analysis (EDA)**: 
   - Memvisualisasikan 10 pekerjaan dan spesialisasi teratas.
   - Menganalisis distribusi tipe pekerjaan (*Full-time*, *Contract*, dll).
   - Memetakan distribusi geografis lowongan di berbagai kota dan provinsi.
   - Menganalisis pekerjaan dengan gaji tertinggi dan distribusi rata-rata gaji.
   - Mengidentifikasi *top recruiters*.

## 🚀 Cara Menjalankan
1. *Clone* repositori ini:
   ```bash
   git clone https://github.com/Arfiadi/jobstreet-data-analysis.git
   ```
2. Pastikan kamu sudah menginstal *dependencies* yang diperlukan (`pandas`, `matplotlib`, `seaborn`).
3. Buka file `Analisis_data_jobstreet.ipynb` menggunakan Jupyter Notebook atau VS Code untuk melihat kode dan analisis lengkap.
