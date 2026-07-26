# Wikipedia Data Collection - Renewable Energy Topics

Tools Python yang mengumpulkan artikel Wikipedia berbahasa Indonesia tentang energi terbarukan ("Energi Terbarukan"), menyimpannya ke dalam file CSV terstruktur, dan melakukan analisis teks dasar (jumlah kata per artikel dan kata yang paling sering muncul) sebagai data persiapan untuk project NLP lanjutan.

> *Project ini dikerjakan sebagai tugas mata kuliah Natural Language Processing pada semester 7, dikerjakan secara individu.*

## Tech Stack

- Python
- wikipedia / wikipedia-api - pengambilan konten Wikipedia
- csv (standard library) - ekspor data terstruktur
- re, collections.Counter - analisis teks

## Cara Menjalankan

### Prerequisites
- Python 3.x

### Instalasi

```bash
# 1. Clone repository
git clone https://github.com/DanuSetiawan05/Wikipedia-Data-Collection-Renewable-Energy-Topics.git
cd Wikipedia-Data-Collection-Renewable-Energy-Topics

# 2. Install dependencies
pip install wikipedia wikipedia-api

# 3. Jalankan notebook
jupyter notebook wikipedia_renewable_energy_collector.ipynb
```

## Cara Kerja

1. Mencari artikel Wikipedia (berbahasa Indonesia) terkait "Energi Terbarukan", dengan penanganan halaman disambiguasi dan halaman yang tidak ditemukan
2. Menyimpan artikel yang terkumpul (judul, URL, konten lengkap, ringkasan) ke dalam file CSV dengan delimiter titik koma
3. Membaca ulang file CSV yang sudah diekspor untuk verifikasi integritas data, lalu menghitung jumlah kata per artikel
4. Mengidentifikasi 10 kata yang paling sering muncul di seluruh artikel (setelah menghapus stopword Bahasa Indonesia)

## Dataset

Dataset terdiri dari 10 artikel Wikipedia berbahasa Indonesia terkait energi terbarukan, termasuk artikel utama "Energi terbarukan" dan topik-topik terkait (energi tak terbarukan, sumber energi spesifik, dll). 

## Struktur Project

```
wikipedia_renewable_energy_collector.ipynb   - Notebook analisis utama
artikel_energi_terbarukan.csv                - Dataset hasil pengumpulan
```

## Langkah Selanjutnya untuk Analisis NLP

1. Text preprocessing - cleaning, tokenization, penghapusan stopword
2. Ekstraksi kata kunci / analisis TF-IDF
3. Topic modeling (LDA atau BERTopic) untuk menemukan subtopik
4. Visualisasi word cloud
5. Eksperimen peringkasan teks atau klasifikasi

## Author

Muhammad Danu Setiawan

## Lisensi

Project ini bersifat open source dan tersedia untuk keperluan pembelajaran. Konten Wikipedia yang dikumpulkan tetap berlisensi CC BY-SA; mohon cantumkan atribusi ke Wikipedia saat menggunakan ulang dataset ini.
