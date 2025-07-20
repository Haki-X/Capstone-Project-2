# Analisis Efisiensi Armada Taksi NYC (Januari 2023)

## 1. Latar Belakang Proyek

Proyek ini merupakan studi kasus analisis data yang bertujuan untuk meningkatkan efisiensi operasional sebuah perusahaan taksi di New York City. Dengan menganalisis data perjalanan NYC Green Taxi untuk bulan Januari 2023, kita dapat menemukan *insight* yang dapat ditindaklanjuti untuk mengurangi waktu kosong pengemudi, memaksimalkan pendapatan, dan mengurangi biaya operasional.

Hasil akhir dari analisis ini disajikan dalam bentuk Jupyter Notebook, dashboard Tableau interaktif, dan sebuah presentasi yang ditujukan untuk para *stakeholder*.

---

## 2. Pertanyaan Bisnis

Analisis ini dirancang untuk menjawab tiga pertanyaan kunci:

* **Identifikasi Jam Sibuk dan Area Permintaan Tinggi:** Kapan dan di mana permintaan taksi paling tinggi?
* **Optimalisasi Rute:** Rute mana yang paling sering ditempuh dan paling menguntungkan ("Rute Emas")?
* **Pengukuran Efisiensi Armada:** Bagaimana cara mengukur efisiensi armada secara keseluruhan dengan metrik yang andal?

---

## 3. Metodologi Analisis

Proses analisis data dilakukan melalui beberapa tahapan utama:

1.  **Pembersihan Data:**
    * Memfilter data hanya untuk periode Januari 2023.
    * Menangani nilai yang hilang (*missing values*), tipe data yang tidak sesuai, dan nilai negatif yang tidak logis pada kolom finansial.
    * Menghapus *outlier* dan anomali data berdasarkan logika bisnis, seperti perjalanan dengan kecepatan yang tidak masuk akal.

2.  **Rekayasa Fitur (*Feature Engineering*):**
    * Membuat kolom turunan seperti `trip_duration_minutes`, `pickup_hour`, `day_of_week`, dan `route`.
    * Mengembangkan metrik efisiensi utama: **"Total Jam Produktif Harian"** sebagai KPI.

3.  **Analisis Eksploratif (EDA):**
    * Menggunakan statistik deskriptif untuk memahami distribusi data.
    * Menganalisis korelasi antar variabel numerik menggunakan *heatmap*.

4.  **Visualisasi Data:**
    * Membuat grafik di Python (`Matplotlib` & `Seaborn`) untuk eksplorasi awal.
    * Membangun dashboard interaktif di **Tableau Public** untuk menyajikan temuan kepada audiens bisnis.

---

## 4. Temuan Utama (*Key Insights*)

1.  **Permintaan Sangat Terpusat:** Permintaan taksi tidak acak, melainkan terkonsentrasi pada jam-jam sibuk sore hari (17.00 - 20.00) dan di beberapa lokasi *hotspot* utama yang telah terpetakan.

2.  **Profitabilitas > Popularitas:** Rute yang paling menguntungkan ("Rute Emas") adalah rute-rute dengan jarak tempuh yang lebih jauh, yang belum tentu merupakan rute yang paling sering dilalui.

3.  **Efisiensi Terukur:** Metrik "Total Jam Produktif Harian" berhasil menjadi KPI yang andal untuk melacak produktivitas armada. Analisis menunjukkan adanya pola mingguan yang jelas, dengan puncak produktivitas terjadi pada akhir pekan.

---

## 5. Alat dan Teknologi

* **Bahasa & Library:** Python (Pandas, Matplotlib, Seaborn, GeoPandas)
* **Lingkungan Kerja:** Jupyter Notebook
* **Visualisasi & Dashboard:** Tableau Public
* **Presentasi:** Microsoft PowerPoint / Canva

---

## 6. Isi Repositori

* `Project2_cleaned.ipynb`: Notebook utama yang berisi seluruh proses analisis dari awal hingga akhir.
* `/data_files/`: Folder berisi file-file yang digunakan dan dihasilkan.
    * `NYC TLC Trip Record.csv`: Dataset mentah.
    * `Peta Hotspot.geojson`: File geospasial untuk pemetaan.
    * `NYC TLC January 2023.xlsx`: Data perjalanan bersih untuk Tableau.
    * `data_harian.xlsx`: Data produktivitas harian untuk Tableau.
    * `Project_2_cleaned`: Analisis pada Notebook.


---

## 7. Cara Menggunakan

1.  *Clone* repositori ini ke komputer lokal Anda.
2.  Pastikan semua *library* Python yang dibutuhkan (`pandas`, `matplotlib`, `seaborn`, `geopandas`) sudah terinstal.
3.  Jalankan sel-sel kode di dalam `Project2_cleaned.ipynb` secara berurutan.
4.  Buka dashboard Tableau Public interaktif melalui tautan ini: **[https://public.tableau.com/views/Project_2_17529086126170/Dashboard1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link]**

---

Dianalisis oleh: **[Abdus Salam Baihaqy Achmad]**
