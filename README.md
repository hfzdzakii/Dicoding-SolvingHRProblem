# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000. Ia memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. (Fiction Scenario)

### Permasalahan Bisnis

Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini terlihat dari tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

### Cakupan Proyek

Melakukan analisis data dengan limitasi **dataset yang diberikan**. Hal yang dianalisis antara lain:
- Faktor yang menyebabkan karyawan meninggalkan perusahaan.
- Hubungan sebab akibat dari variabel bebas (faktor penyebab atrisi karyawan) dengan variabel terikat (atrisi-nya seorang karyawan).
- Alasan logis yang menjadi penyebab atrisi karyawan.
- Hal yang bisa dilakukan perusahaan **(company action-oriented)** untuk mengurangi karyawan yang keluar dari perusahaan.

### Persiapan

Sumber data: [here](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

Setup environment:

```
$ conda create --name myenv "python<3.11"
$ conda activate myenv
$ pip install -r requirements.txt

```

## Business Dashboard

- Gambar Dashboard:
    1. haztsu-dashboard-page-1.jpg
    2. haztsu-dashboard-page-2.jpg

- Metadata dashboard untuk Metabase:
    - ./metabase.db/metabase.mv.db

*Membaca dari kiri-kanan & atas-bawah*

1. Current Overall Attrition Rate:

    Ratio atrisi di perusahaan saat ini

2. High Risk Employee Leave Count:

    Jumlah karyawan yang **kemungkinan besar** akan segera keluar

3. At Risk Employee Leave Count:

    Jumlah karyawan yang **memiliki risiko kemungkinan** akan segera keluar

4. Overtime vs Job Satisfactory:

    Visualisasi heatmap antara karyawan yang <u>bekerja lembur</u> & <u>kepuasan bekerja</u> terhadap rasa ingin meninggalkan perusahaan. Cukup jelas terlihat: 

    - **Tidak lembur** & rasa puas yang tinggi = tingkat **atrisi rendah** & bertahan di perusahaan tinggi
    - **Lembur** & rasa puas yang rendah = tingkat **atrisi tinggi** & bertahan di perusahaan rendah

5. Stock Option Level vs Attrition:

    Visualisasi bar chart stack antara kompensasi opsi saham karyawan dengan tingkat atrisi karyawan. Bisa dilihat:

    - Semakin rendah opsi saham yang bisa dimiliki oleh karyawan, semakin tinggi kemungkinan karyawan tersebut ingin keluar
    - Kecuali tingkat opsi "High", tingkat karyawan ingin keluar melebihi opsi "Low" dan "Medium"

6. Relation Satisfaction vs Attrition:

    Visualisasi multiple bar chart antara tingkat kepuasan hubungan kerja dengan atrisi karyawan. Bisa dilihat:

    - Perusahaan Jaya Jaya Maju merupakan perusahaan yang baik karena tingkat hubungan kerja antarkaryawan yang memuaskan sangat tinggi
    - Secara kuantitas, lebih banyak karyawan yang keluar dari perusahaan karena merasa hubungan kerja yang rendah

    6.1. Low-Medium-High-Very High Satisfaction Attrition Ratio:

    Ratio atrition karyawan dengan kepuasan rendah dari berbagai tingkat kepuasan. 

8. dfs

## Conclusion

Jelaskan konklusi dari proyek yang dikerjakan.

### Rekomendasi Action Items (Optional)

Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

- action item 1
- action item 2
