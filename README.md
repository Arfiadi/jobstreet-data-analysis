# Analisis Data Lowongan Pekerjaan Bidang Data di JobStreet Indonesia

Proyek ini merupakan **Proyek Akhir Mata Kuliah Pemrosesan Data (Semester 2)** di Program Studi Sains Data Terapan, Politeknik Elektronika Negeri Surabaya (PENS). Proyek ini bertujuan untuk mengekstrak, membersihkan, dan menganalisis data lowongan pekerjaan di bidang *Data* dari situs JobStreet Indonesia untuk memahami tren pasar kerja.

## 👥 Tim Peneliti
- Ziyad Yusuf Fauzan (3324600001)
- Arfi Adi Nugroho (3324600019)
- Muhammad Ikhwan F. (3324600002)

## 📌 Latar Belakang & Tujuan
Dengan meningkatnya kebutuhan akan tenaga profesional di bidang data (Data Analyst, Data Scientist, Data Engineer) di Indonesia, proyek ini bertujuan untuk memberikan wawasan mendalam mengenai:
- Pekerjaan spesifik yang paling banyak dicari.
- Distribusi gaji berdasarkan peran dan lokasi geografis.
- Perusahaan perekrut yang paling aktif di bidang data.
- Spesialisasi dan komitmen waktu (Full-time vs Kontrak) yang mendominasi.

## 📂 Dataset
Data dikumpulkan menggunakan metode **Web Scraping** (via WebScraper.io) pada 1 Juni 2025 dengan kata kunci "data" di situs JobStreet Indonesia.
- **Total Data Awal:** ~12.105 lowongan (Scraping berhasil mengambil sampel representatif sebanyak 878 baris data).
- `jobstreet_data_jobs_hasilscraping.xlsx`: Dataset mentah hasil scraping.
- `jobstreet_data_jobs_final.xlsx`: Dataset yang telah melalui proses *Data Cleaning* dan *Preprocessing*.

## 🛠️ Alur Pemrosesan Data (*Data Preprocessing*)
Proses pembersihan data dilakukan di dalam `Analisis_data_jobstreet.ipynb` meliputi:
1. **Penanganan Missing Values**: Mengisi nilai kosong dengan `unknown` pada fitur kategorikal dan mempertahankan `NaN` pada data gaji.
2. **Normalisasi Job Title**: Penyeragaman huruf kecil dan pembersihan karakter.
3. **Parsing Gaji**: Memecah string gaji menjadi fitur numerik `min_salary` dan `max_salary`.
4. **Ekstraksi Lokasi**: Memecah string lokasi menjadi level kota (`city`) dan provinsi (`province`).
5. **Konversi Waktu**: Mem-*parsing* fitur `posted_date` menjadi format *datetime*.

## 📊 Insight Utama (*Exploratory Data Analysis*)
1. **Dominasi Peran**: **Data Analyst** adalah posisi dengan permintaan tertinggi di pasar kerja data Indonesia.
2. **Jenis Pekerjaan**: Mayoritas perusahaan memprioritaskan pekerja **Full-time** dibandingkan pekerja kontrak/temporer.
3. **Lokasi Terpusat**: Pasar kerja data Indonesia masih sangat terpusat di **Jakarta Raya** (khususnya Jakarta Selatan).
4. **Rentang Gaji**: Mayoritas kompensasi dasar berada pada rentang **Rp 5.000.000 - Rp 9.000.000**. Namun, spesialisasi seperti *Analis Bisnis/Sistem* di Jakarta Selatan dapat mencapai *outlier* di atas Rp 25.000.000.
5. **Top Recruiter**: Perusahaan seperti PT. TRANSNOVASI BANGUN PERSADA dan PT. Satya Langgeng Sentosa termasuk di antara perekrut paling aktif untuk posisi data.

## 🚀 Cara Menjalankan
1. *Clone* repositori ini:
   ```bash
   git clone https://github.com/Arfiadi/jobstreet-data-analysis.git
   ```
2. Pastikan sudah menginstal pustaka yang dibutuhkan (`pandas`, `matplotlib`, `seaborn`).
3. Buka dan jalankan `Analisis_data_jobstreet.ipynb` menggunakan Jupyter Notebook atau IDE pilihanmu (VS Code/PyCharm).

---
*Proyek ini disusun sebagai bagian dari pemenuhan tugas akhir mata kuliah Pemrosesan Data Semester 2 (TA 2024/2025) di bawah bimbingan Ibu Alfi Fadliana S.Si., M.Stat.*
