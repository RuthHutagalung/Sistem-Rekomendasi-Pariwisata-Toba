# Sistem Rekomendasi Pariwisata Toba 

# Project Overview
![image](https://github.com/user-attachments/assets/a88c23f3-7451-488b-9d9f-b9d6b1b984c9)

Proyek Sistem Rekomendasi Pariwisata Toba bertujuan untuk menciptakan sebuah mesin rekomendasi yang dipersonalisasi, yang dirancang untuk industri pariwisata di kawasan Danau Toba. Sistem ini bertujuan untuk memberikan rekomendasi destinasi wisata, akomodasi, dan aktivitas yang relevan kepada pengguna berdasarkan preferensi mereka, interaksi sejarah, dan fitur konten menggunakan dua teknik populer dalam sistem rekomendasi: Collaborative Filtering (CF) dan Content-Based Filtering (CBF). Sistem ini diharapkan dapat meningkatkan pengalaman pengguna dengan memberikan rekomendasi perjalanan yang sesuai dengan kebutuhan dan minat spesifik wisatawan.

---

### 1️⃣ **Business Understanding**
Toba Tourism Recommendation System adalah proyek yang bertujuan untuk meningkatkan pengalaman wisatawan yang berkunjung ke kawasan Danau Toba melalui sistem rekomendasi yang dipersonalisasi. Kawasan Danau Toba, yang terkenal sebagai salah satu destinasi wisata utama di Indonesia, memiliki potensi besar untuk menarik lebih banyak wisatawan domestik maupun internasional. Namun, dengan berbagai macam pilihan destinasi wisata, akomodasi, dan aktivitas yang tersedia, wisatawan sering kali merasa kesulitan untuk menemukan rekomendasi yang sesuai dengan minat dan preferensi pribadi mereka.

**Tujuan Bisnis**:
- Meningkatkan Pengalaman Pengguna dengan memberikan rekomendasi yang relevan dan personal.
- Mendukung Pariwisata Lokal dengan mempromosikan destinasi yang kurang dikenal.
- Meningkatkan Keterlibatan Pengguna melalui rekomendasi yang lebih tepat dan menarik.

---

### 2️⃣ **Data Understanding**

Dataset ini berisi informasi mengenai pengguna, destinasi wisata, dan interaksi antara keduanya. Berikut adalah elemen-elemen utama:

1. **User Data**:
   - **user_id**: Identifikasi unik untuk pengguna.
   - **age**: Usia pengguna.
   - **gender**: Jenis kelamin pengguna.
   - **location**: Lokasi pengguna.

2. **Item Data**:
   - **item_id**: Identifikasi unik untuk destinasi atau aktivitas.
   - **name**: Nama destinasi atau aktivitas.
   - **category**: Kategori seperti wisata alam, budaya, kuliner.
   - **location**: Lokasi destinasi wisata.
   - **rating**: Rating yang diberikan pengguna pada item.

3. **Interaction Data**:
   - **user_id, item_id**: Menunjukkan interaksi antara pengguna dan destinasi/aktivitas tertentu melalui pemberian rating atau review. 

---

### 3️⃣ **Data Preparation**
1. **Penanganan Nilai Hilang**: Mengisi atau menghapus data yang hilang pada kolom seperti usia, kategori, dan rating.
2. **Encoding Kategorikal**: Mengubah kolom kategori (misal, jenis destinasi) menjadi format numerik menggunakan **one-hot encoding** atau **label encoding**.
3. **Normalisasi Data**: Menormalkan kolom rating untuk skala seragam menggunakan **Min-Max scaling** atau **Z-score**.
4. **Pemisahan Data**: Membagi data menjadi **training (70%)**, **validation (15%)**, dan **test (15%)** untuk melatih dan menguji model.

---

### 4️⃣ **Modeling and Result**
### 5️⃣ **Model Evaluation**
