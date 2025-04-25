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

`Run semua cell pada file prediction.ipynb`

Hasil deployemnt juga bisa bisa diakses pada link [berikut](https://huggingface.co/spaces/hfzdzakii/EmployeeAttritionPrediction).


## Business Dashboard

- Gambar Dashboard:
    1. haztsu-dashboard-page-1.jpg
    2. haztsu-dashboard-page-2.jpg

- Metadata dashboard untuk Metabase:
    - ./metabase.db/metabase.mv.db

*Membaca dari kiri-kanan & atas-bawah*

1. Current Overall Attrition Rate:

    Rasio atrisi di perusahaan saat ini

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

    - Low-Medium-High-Very High Satisfaction Attrition Ratio: Rasio atrisi karyawan dengan kepuasan rendah dari berbagai tingkat kepuasan

    - Dapat dilihat kepuasan "Low" memiliki tingkat atrisi karyawan tertinggi

7. Environment Satisfaction vs Year with Current Manager - Attrition:

    Visualisasi chart pie antara kepuasan lingkungan dengan tahun bersama manajer untuk karyawan yang keluar dari perusahaan. Bisa dilihat:

    - Terdapat total 179 karyawan yang ingin meninggalkan perusahaan

    - Kebanyakan dari mereka hanya bertahan 0-5 tahun dengan perasaan kepuasan lingkungan yang rendah

8. Environment Satisfaction vs Year with Current Manager - Retained

9. Environment Satisfaction vs Year with Current Manager - No Data

## Conclusion

Projek ini berhasil menentukan faktor yang menyebabkan tingginya rasio atrisi di Perusahaan Jaya Jaya Maju. 

Tidak asal memilih, semua faktor berasal dari hasil research mandiri dan membaca artikel serta jurnal ilmiah. Fitur yang digunakan untuk prediksi model juga telah dioptimasi menggunakan perhitungan P-Values Hypothesis Testing serta ML model yang dipilih adalah yang terbaik dari hasil experimen.

1. Identifikasi faktor yang menyebabkan karyawan pergi dari perusahaan

    - Terkait kompensasi : `StokOptionLevel`
    - Terkait perusahaan : `EnvironmentSatisfaction`, `OverTime`, `JobSatisfaction`, `RelationshipSatisfaction`
    - Terkait pengembangan karir : `YearsSinceLastPromotion`, `TotalWorkingYears`, `NumCompaniesWorked`, `YearsWithCurrManager`

2. Metabase dashboard

    - haztsu-dashboard-page-1.jpg
    - haztsu-dashboard-page-2.jpg

3. Gradio deployemnt 

    Bisa diakses lewat [sini](https://huggingface.co/spaces/hfzdzakii/EmployeeAttritionPrediction)

### Rekomendasi Action

1. Minimalisir karyawan untuk bekerja lembur (bila memang tidak benar-benar diperlukan) dan tingkatkan kepuasan berkerja. Sehingga, tingkat atrisi bisa menurun.

2. Berikan opsi kepemilikan saham ke tingkat "Low" dan "Medium" bagi karyawan yang layak mendapat peningkatan. Hindari peningkatan ke "High" untuk mencegah atrisi karyawan.

3. Evaluasi faktor kepuasan hubungan dalam perusahaan. Baik hubungan antarkarywan atau atasan dengan bawahan.

4. Perhatikan karyawan baru (0-5 tahun berkerja) agar mereka bisa beradaptasi dan dimohon untuk manajerial mendukung dan membantu karywan baru agar betah.
