# ecommerce-customer-revenue-retention-analysis
Customer revenue and retention analysis using Python (RFM, cohort, and business insights for e-commerce).

# Customer Revenue & Retention Analysis for E-Commerce

## 1. Latar Belakang Bisnis

Dalam industri e-commerce, pertumbuhan pendapatan jangka panjang sangat bergantung pada kemampuan perusahaan untuk:
1) memahami perilaku pelanggan,
2) mengidentifikasi segmen bernilai tinggi, dan
3) mengelola retensi secara strategis.

Proyek ini menyajikan analisis menyeluruh terhadap data transaksi e-commerce untuk menjawab pertanyaan kunci terkait sumber pendapatan, loyalitas pelanggan, serta pola pembelian berulang. Seluruh analisis dilakukan menggunakan Python sebagai alat utama pengolahan data.

## 2. Tujuan Analisis

Proyek ini dirancang untuk menjawab beberapa pertanyaan bisnis berikut:

- Siapa pelanggan dengan kontribusi pendapatan terbesar?
- Sejauh mana pelanggan melakukan pembelian berulang (retention & repeat purchase)?
- Bagaimana distribusi pendapatan berdasarkan produk, kategori, dan periode waktu?
- Bagaimana segmentasi pelanggan berdasarkan metrik RFM (Recency, Frequency, Monetary)?
- Rekomendasi apa yang dapat diambil manajemen untuk meningkatkan CLV (Customer Lifetime Value)?

## 3. Data

- Sumber: Public e-commerce dataset (multi-tabel: orders, customers, items, payments, dsb.).
- Unit analisis utama: transaksi per pelanggan.
- Contoh variabel:
  - `customer_id`, `order_id`, `order_purchase_timestamp`
  - `price`, `freight_value`, `payment_value`
  - `product_category`, dsb.
- Data telah dianonimkan. Meskipun demikian, struktur dan kompleksitasnya merepresentasikan konteks bisnis riil.

Catatan kritis:
- Terdapat potensi outlier (harga ekstrem, durasi pengiriman tidak wajar).
- Terdapat missing values pada beberapa atribut.
- Periode data terbatas, sehingga interpretasi tren jangka panjang harus dilakukan secara hati-hati.

## 4. Metodologi Singkat

1. **Data Cleaning & Preparation**
   - Menghapus duplikasi.
   - Menangani nilai hilang.
   - Membentuk data mart pelanggan (agregasi transaksi per pelanggan).

2. **Exploratory Data Analysis (EDA)**
   - Distribusi pendapatan per pelanggan.
   - Pola pembelian berdasarkan waktu.
   - Analisis kontribusi produk/kategori terhadap total revenue.

3. **RFM Segmentation**
   - Perhitungan Recency, Frequency, Monetary per pelanggan.
   - Skoring dan pengelompokan sederhana (misal: Champion, Loyal, At Risk, Hibernating).
   - Evaluasi apakah segmen tertentu mendominasi pendapatan.

4. **Cohort & Retention Overview (Opsional namun direkomendasikan)**
   - Pembentukan cohort berdasarkan bulan pembelian pertama.
   - Menghitung persentase pelanggan yang tetap aktif pada bulan-bulan berikutnya.

5. **Business Insight & Rekomendasi**
   - Menghubungkan temuan kuantitatif dengan keputusan bisnis yang konkret.

## 5. Temuan Utama (Outline)

Beberapa jenis insight yang ditargetkan (akan diisi berdasarkan hasil analisis):

- Proporsi pendapatan yang terkonsentrasi pada segmen pelanggan tertentu.
- Identifikasi pelanggan dengan nilai transaksi tinggi namun berisiko churn.
- Pola waktu pembelian yang dapat dimanfaatkan untuk campaign periodik.
- Kategori produk dengan kontribusi tertinggi terhadap revenue dan repeat order.

## 6. Rekomendasi Bisnis (Outline)

Contoh arah rekomendasi yang akan dikembangkan:

- Program retensi khusus untuk segmen "High Value" dan "Loyal Customers".
- Optimalisasi promo pada periode dengan potensi penjualan tinggi.
- Prioritas layanan dan SLA pengiriman untuk segmen bernilai tinggi.

## 7. Teknologi yang Digunakan

- **Python**: pandas, numpy, matplotlib, seaborn, plotly
- **Jupyter Notebook** untuk EDA dan visualisasi
- (Opsional) **SQL** untuk eksplorasi awal data
- **GitHub** sebagai media dokumentasi dan version control

## 8. Cara Menjalankan

1. Clone repository ini.
2. Letakkan dataset pada folder `data/raw/`.
3. Jalankan notebook `notebooks/01_eda_rfm_retention.ipynb` secara berurutan.
4. Hasil grafik dan tabel ringkasan akan tersimpan pada folder `outputs/`.
