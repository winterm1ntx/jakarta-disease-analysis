# Analisis Beban Penyakit di DKI Jakarta (2023-2025)

## Latar Belakang

Jakarta terdiri dari 6 wilayah administratif dengan karakteristik demografis berbeda. Memahami distribusi kasus penyakit antar wilayah dapat membantu identifikasi area yang membutuhkan perhatian kesehatan lebih besar.

## Problem Statement

Menganalisis distribusi dan variasi jumlah kasus penyakit menular antar wilayah administratif di DKI Jakarta periode 2023-2025, guna mengidentifikasi wilayah yang membutuhkan perhatian kesehatan masyarakat lebih besar.

## Pertanyaan Riset (Utama)

Apakah jumlah kasus tiap jenis penyakit berbeda signifikan antar wilayah di Jakarta selama periode 2023-2025?

## Rumusan Masalah

1. Jenis penyakit apa yang paling bervariasi jumlah kasusnya antar wilayah?
2. Wilayah mana yang secara konsisten punya jumlah kasus tinggi di banyak jenis penyakit?
3. Apakah ada tren naik/turun dari tahun 2023 ke 2025 untuk penyakit tertentu?
4. Apakah wilayah dengan kasus DBD tinggi juga cenderung tinggi di penyakit menular lain? (tidak dieksplorasi lebih lanjut — lihat bagian Keterbatasan)

## Sumber Data

Satu Data Jakarta — Jumlah Kasus Penyakit Menurut Kabupaten/Kota dan Jenis Penyakit di Provinsi DKI Jakarta (2023-2025), diterbitkan oleh Dinas Kesehatan 
Provinsi DKI Jakarta.

## Metodologi

1. Data Cleaning: standardisasi label penyakit yang tidak konsisten antar tahun (PNEUMONIA1 → PNEUMONIA), verifikasi definisi kategori data terhadap deskripsi resmi sumber data.
2. Uji Statistik: Kruskal-Wallis test untuk menguji perbedaan jumlah kasus tiap jenis penyakit antar wilayah (Kepulauan Seribu dikecualikan karena karakteristik demografis yang jauh berbeda).
3. Analisis Deskriptif: perbandingan rata-rata kasus per wilayah dan tren tahunan untuk penyakit yang terbukti signifikan.

## Temuan Utama

Dari 10 jenis penyakit yang diuji, 4 penyakit menunjukkan perbedaan jumlah kasus yang signifikan antar wilayah (p-value < 0.05): TB Paru, Kusta, AIDS kasus baru, dan Malaria.

  - TB Paru memiliki variasi terbesar antar wilayah, dengan pola persebaran yang landai (tersebar merata, tidak ada wilayah yang jomplang ekstrem).
  - Kusta dan Malaria menunjukkan pola hotspot — terkonsentrasi tajam di satu wilayah (Kusta di Jakarta Pusat, Malaria di Jakarta Timur).
  - Jakarta Timur adalah wilayah paling konsisten memiliki beban kasus tinggi, unggul di 2 dari 4 penyakit signifikan (TB Paru dan Malaria).
  - Tren 2023-2025: AIDS kasus baru menurun konsisten, sementara Malaria meningkat konsisten hampir dua kali lipat.

## Rekomendasi

- Jakarta Timur dapat menjadi prioritas program kesehatan masyarakat yang bersifat menyeluruh.
- Jakarta Pusat (Kusta) dan Jakarta Timur (Malaria) berpotensi diuntungkan dari intervensi yang lebih tertarget.
- Peningkatan tren Malaria perlu diinvestigasi lebih lanjut.

## Keterbatasan

- Data menggunakan angka kasus absolut, belum dinormalisasi terhadap jumlah penduduk per wilayah.
- Kepulauan Seribu dikecualikan dari uji statistik karena outlier demografis.
- Sample size relatif kecil (3 titik data per tahun per wilayah).
- Rumusan masalah #4 (korelasi DBD) tidak dieksplorasi karena DBD tidak signifikan pada uji statistik utama.

## Pengembangan Lanjutan

- Normalisasi data terhadap jumlah penduduk per wilayah.
- Eksplorasi data multi-tahun yang lebih panjang untuk validasi tren.

## Tools

- Python (pandas, scipy, matplotlib)
- Jupyter Notebook

## Struktur Repository
├── dataset.xlsx
├── analisis_penyakit_jakarta.ipynb
├── perbandingan_wilayah.png
├── tren_waktu.png
└── README.md
