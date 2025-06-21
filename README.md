🧠 Penambangan Data — Analisis Pola Pembelian Konsumen
Proyek ini merupakan implementasi metode frequent pattern mining dan unsupervised learning untuk menemukan pola tersembunyi dan segmentasi konsumen dalam data transaksi kategori makanan. Studi ini menggunakan teknik seperti Apriori, FP-Growth, dan K-Means Clustering.

📂 Dataset :
Dataset yang digunakan adalah NationalTotalAndSubcategory.csv ('https://www.ers.usda.gov/data-products/weekly-retail-food-sales') yang berisi informasi transaksi harian berdasarkan kategori dan subkategori makanan. Dataset telah melalui proses cleaning dan preprocessing untuk menghilangkan duplikasi, nilai yang tidak relevan, dan untuk menyusun data dalam format yang siap ditambang.

⚙️ Alur Proses
1. 🧹 Data Preprocessing
Pembatasan ukuran data untuk efisiensi (hingga 30.000 baris)

Penghapusan kolom tidak relevan: Variable, Value

Konversi kolom Date ke format datetime

Penyaringan kategori dan subkategori Other

Pembuatan binary transaction matrix dengan teknik one-hot encoding

2. 📊 Exploratory Data Analysis (EDA)
Visualisasi distribusi jumlah transaksi berdasarkan Category dan Subcategory

Pemetaan frekuensi untuk pemahaman awal terhadap pola pembelian

3. 📈 Frequent Pattern Mining
a. Apriori
Menemukan itemset frekuen dengan min_support = 0.02

Menghasilkan aturan asosiasi berdasarkan confidence dan lift

Visualisasi Top-10 Frequent Itemsets

b. FP-Growth
Alternatif cepat dari Apriori untuk itemset besar

Aturan asosiasi diurutkan berdasarkan confidence tertinggi

Penyajian aturan dalam bahasa natural agar lebih interpretatif

4. 📉 K-Means Clustering
Normalisasi data numerik dengan StandardScaler

Penentuan jumlah optimal cluster menggunakan Elbow Method

Pembentukan 3 segmen konsumen:

Cluster 0: Hemat, hanya beli yang esensial

Cluster 1: Konsumen umum, belanja ringan banyak kategori

Cluster 2: Plant-based / natural eater (tinggi konsumsi sayur)

Visualisasi jumlah anggota tiap cluster

🛠️ Tools & Library
Pandas, NumPy — Manipulasi data

Matplotlib, Seaborn — Visualisasi

mlxtend.frequent_patterns — Apriori & FP-Growth

scikit-learn — KMeans & StandardScaler

📌 Insight Penting
Produk dari kategori tertentu cenderung dibeli bersamaan dalam pola tetap (association rules)

Segmen konsumen bisa dikelompokkan dengan baik berdasarkan intensitas dan jenis konsumsi

Teknik data mining mampu mendukung pengambilan keputusan dalam strategi pemasaran dan pengelompokan pelanggan
