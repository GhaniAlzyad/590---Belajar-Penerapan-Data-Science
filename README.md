# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

Jaya Jaya Maju merupakan sebuah perusahaan multinasional besar yang telah berdiri sejak tahun 2000. Saat ini, perusahaan memiliki lebih dari 1000 karyawan yang tersebar di berbagai wilayah operasional. Seiring dengan pertumbuhan perusahaan yang cukup masif, tim HR (Human Resources) menghadapi tantangan besar dalam mengelola sumber daya manusianya, yang berdampak pada stabilitas tenaga kerja perusahaan.

### Permasalahan Bisnis

Terdapat beberapa permasalahan utama yang ingin diselesaikan melalui proyek ini:

1. Tingginya Attrition Rate: Rasio jumlah karyawan yang keluar (resign) dibandingkan dengan total keseluruhan karyawan mencapai angka di atas 10%, yang mana ini merupakan tren yang mengkhawatirkan dan merugikan perusahaan secara operasional maupun finansial.

2. Ketidaktahuan terhadap Faktor Pemicu: Manajer HR kesulitan mengidentifikasi secara pasti faktor-faktor atau variabel apa saja yang paling memengaruhi keputusan seorang karyawan untuk meninggalkan perusahaan.

3. Ketiadaan Alat Pemantauan (Monitoring Tool): Perusahaan belum memiliki sistem atau dashboard yang memudahkan manajemen untuk memonitor metrik-metrik karyawan dan faktor-faktor risiko attrition secara praktis dan interaktif.

### Cakupan Proyek

Untuk menyelesaikan permasalahan di atas, cakupan proyek ini meliputi:

1. Data Preparation & Cleaning: Membersihkan dataset dari missing values (terutama pada kolom target) dan membuang fitur yang tidak relevan.

2. Exploratory Data Analysis (EDA): Menganalisis distribusi data untuk memahami karakteristik demografi dan pekerjaan karyawan.

3. Machine Learning Modeling: Membangun model klasifikasi (menggunakan algoritma Random Forest) untuk memprediksi karyawan yang berpotensi keluar, sekaligus mengekstrak Feature Importance guna mengetahui faktor penyebab utama attrition.

4. Dashboard Creation: Mengembangkan Business Dashboard interaktif menggunakan Streamlit untuk memvisualisasikan faktor-faktor attrition agar mudah dibaca oleh Manajer HR.

### Persiapan

Sumber data: Dataset internal HR perusahaan (employee_data.csv) yang berisi rekam jejak, informasi demografi, kepuasan kerja, dan status pengunduran diri 1470 karyawan.

Setup environment:

# Membuat virtual environment (opsional namun disarankan)
python -m venv env
source env/bin/activate  # Untuk Linux/Mac
# env\Scripts\activate   # Untuk Windows

# Menginstal library yang dibutuhkan
pip install pandas numpy matplotlib seaborn scikit-learn streamlit

## Business Dashboard

Business Dashboard telah dibangun menggunakan Streamlit. Dashboard ini dirancang khusus untuk Manajer HR agar dapat memantau kondisi karyawan secara menyeluruh. Fitur dalam dashboard ini meliputi:

1. KPI (Key Performance Indicators) Utama: Menampilkan total karyawan, jumlah karyawan yang keluar, dan persentase attrition rate terkini.

2. Visualisasi Faktor Utama: Menampilkan grafik perbandingan dari faktor-faktor dominan (seperti pengaruh MonthlyIncome, Age, atau OverTime) terhadap tingkat pengunduran diri karyawan.

3. Identifikasi Risiko: Membantu HR melihat demografi atau departemen mana yang memiliki kerentanan paling tinggi.

## Conclusion

Dari hasil analisis dan pemodelan Machine Learning yang telah dilakukan, dapat disimpulkan bahwa perusahaan memang memiliki tantangan retensi karyawan yang cukup signifikan. Model Random Forest berhasil memetakan pola keluarnya karyawan dan menemukan bahwa keputusan resign tidak terjadi secara acak, melainkan sangat dipengaruhi oleh beberapa faktor krusial. Faktor-faktor dominan seperti Gaji Bulanan (Monthly Income), Usia (Age), Beban Lembur (OverTime), dan Jarak dari Rumah (Distance From Home) seringkali menempati urutan teratas sebagai alasan di balik tingginya attrition rate di Jaya Jaya Maju.

### Rekomendasi Action Items (Optional)

Berdasarkan temuan data, berikut adalah beberapa rekomendasi tindakan yang dapat dilakukan oleh Manajer HR dan Manajemen Perusahaan:

1. Mengevaluasi Struktur Kompensasi: Melakukan peninjauan ulang terhadap Monthly Income (gaji bulanan) karyawan, terutama bagi mereka yang berada di level junior atau memiliki skill yang sangat kompetitif di pasar, untuk memastikan gaji yang diberikan sudah sesuai dengan standar industri.

2. Mengelola Beban Kerja dan Lembur: Mengontrol kebijakan OverTime (lembur) dengan ketat. Karyawan yang terlalu sering lembur rentan terhadap burnout. Perusahaan bisa mempertimbangkan penambahan staf di departemen yang overloaded.

3. Program Engagement untuk Karyawan Muda: Karena faktor Usia (Age) biasanya cukup berpengaruh (karyawan muda cenderung lebih sering berpindah kerja), buat program pengembangan karir atau mentorship yang jelas untuk meningkatkan loyalitas mereka.

4. Fleksibilitas Kerja: Mempertimbangkan kebijakan Work From Anywhere (WFA) atau hybrid bagi karyawan yang jarak rumahnya jauh (Distance From Home tinggi) untuk mengurangi tingkat stres akibat perjalanan harian.
