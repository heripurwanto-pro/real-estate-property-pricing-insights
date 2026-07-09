# Real Estate Property Pricing Insights

Proyek analisis data ini bertujuan untuk melakukan pembersihan, transformasi, dan pemetaan karakteristik pasar real estate di wilayah Jabodetabek. Melalui pendekatan berbasis data, proyek ini memberikan rekomendasi strategis bagi tim manajemen untuk penentuan harga proyek properti baru agar tetap kompetitif di pasar massal maupun premium.

## Tujuan Proyek
* Pembersihan Data: Mengeliminasi data ekstrem (outliers) harga rumah agar analisis statistik tidak terdistorsi.
* Imputasi Data: Menangani nilai kosong (missing values) pada variabel luas tanah tanpa kehilangan informasi pasar yang berharga.
* Feature Engineering: Membuat indikator metrik baru Harga_per_Meter untuk mengukur efisiensi nilai investasi properti.
* Agregasi & Visualisasi: Memetakan karakteristik harga pasar berdasarkan sebaran wilayah geografis.

---

## Langkah Preprocessing dan Kode Python
Proses pengolahan data dilakukan sepenuhnya menggunakan Python (Pandas, Matplotlib, dan Seaborn) secara runtut:

1. Deteksi Outlier: Menetapkan ambang batas harga wajar menggunakan metode Interquartile Range (IQR). Properti di atas Rp 4.440.639.247,50 diidentifikasi sebagai data pencilan.
2. Data Cleaning: Menghapus 5 data outlier ekstrem (termasuk PROP-004 senilai Rp 18,3 M dan PROP-077 senilai Rp 31,8 M). Ukuran dataset terkoreksi stabil dari 85 menjadi 80 baris bersih.
3. Handling Missing Values: Mengamankan 11 baris data kosong (13% informasi) pada kolom luas tanah dengan menggunakan teknik Imputasi Median ke angka 120.0 m2.
4. Feature Engineering: Membuat kolom baru secara otomatis dengan rumus pembagian antara Harga Jual Rumah dengan Luas Tanah.

---

## Ringkasan Temuan dan Analisis Karakteristik Pasar

Setelah proses pembersihan data selesai dilakukan, bias data akibat nilai ekstrem berhasil dieliminasi. Statistik pasar kini merefleksikan kondisi riil di lapangan:

* Daya Beli Riil: Mayoritas pasar aktif (>50%) stabil di bawah Rp 1,53 Miliar (Nilai Median). Pasca eliminasi anomali aset premium, rata-rata pasar terkoreksi normal pada Rp 1,54 Miliar.
* Efisiensi Harga Geografis (Agregasi): Bogor memimpin nilai investasi tanah paling premium dengan rata-rata Rp 15,11 Juta / m2, disusul oleh Depok sebesar Rp 14,80 Juta / m2. Tangerang dan Bekasi memiliki rata-rata harga per meter lebih rendah (~Rp 13,5 Juta / m2) karena sebaran luas tanah di kedua wilayah tersebut cenderung jauh lebih besar.
* Polarisasi Wilayah Konsumen (Korelasi): Pemetaan data menunjukkan Tangerang dan Bekasi mendominasi segmen premium (Rp 2,0 M - Rp 3,0 M). Sebaliknya, Bogor dan Depok menguasai pasar massal di bawah Rp 1,5 Miliar. Luas bangunan bukan penentu tunggal; faktor lokasi sangat dominan di mana aset kecil di Tangerang/Bekasi memiliki nilai pasar setara atau lebih tinggi dibanding aset besar di wilayah Bogor.

---

## Rekomendasi Aksi Bisnis
Manajemen wajib memisahkan strategi penetapan harga (pricing strategy) berdasarkan segmentasi wilayah:
1. Segmen Massal (Volume Driven): Gunakan basis harga di bawah Rp 1,5 Miliar untuk wilayah Bogor dan Depok demi mengejar volume penjualan cepat dan efisiensi perputaran modal.
2. Segmen Premium (Margin Driven): Alokasikan pengembangan cluster premium dengan target harga di atas Rp 2 Miliar khusus untuk area pengembangan Tangerang dan Bekasi guna memaksimalkan profitabilitas perusahaan.

---

## Struktur Repositori
* tugas_besar_heripurwanto.ipynb : Jupyter Notebook berisi kode lengkap preprocessing dan visualisasi final.
* README.md : Dokumentasi utama portofolio proyek.
