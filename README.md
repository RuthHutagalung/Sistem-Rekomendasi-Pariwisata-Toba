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
### **Collaborative Filtering with Jaccard Similarity**

Salah satu metode dalam CF adalah menggunakan Jaccard Similarity untuk mengukur kemiripan antara pengguna atau item. Tim memilih untuk mengukur kemiripan menggunakan item.
   
**Langkah-langkah:**
- Membangun User-Item Matrix: Data interaksi (misalnya, rating atau klik) antara pengguna dan item digunakan untuk membangun matriks interaksi pengguna-item.
- Menghitung Jaccard Similarity: Berdasarkan matriks, dihitung kemiripan antar item atau antar pengguna menggunakan rumus Jaccard.
- Membuat Rekomendasi: Berdasarkan nilai kemiripan yang dihitung, rekomendasi diberikan kepada pengguna berdasarkan item yang paling mirip dengan item yang sudah mereka pilih sebelumnya.

### **Result**
Gambar 1. Rekomendasi Top 5 Tempat Pariwisata Toba
![WhatsApp Image 2024-12-08 at 08 08 08_cdac1294](https://github.com/user-attachments/assets/5475df77-70da-4302-b108-a61c3164accc)

Gambar 2. Rekomendasi Top 10 Tempat Pariwisata Toba
![WhatsApp Image 2024-12-08 at 08 08 31_149b4636](https://github.com/user-attachments/assets/eabe1aba-7bdb-465d-be80-579d35ee3d96)



### **Content-Based Filtering with Cosine Similarity**
Content-Based Filtering (CBF) merekomendasikan item (seperti destinasi wisata atau aktivitas) berdasarkan kesamaan konten antara item yang sudah disukai pengguna dengan item lainnya.
Cosine Similarity digunakan untuk mengukur seberapa mirip dua item berdasarkan fitur-fitur konten mereka, seperti kategori, deskripsi, atau rating.

**Langkah-langkah:**

- Membangun Item-Feature Matrix: Setiap item (misalnya destinasi wisata) diwakili oleh vektor fitur yang menggambarkan karakteristik item, seperti kategori dan deskripsi.
- Menghitung Cosine Similarity: Menghitung kemiripan antara item yang sudah disukai pengguna dengan item lainnya menggunakan Cosine Similarity.

### **Result**
Gambar 3. Rekomendasi Top 5 Tempat Pariwisata Toba
![WhatsApp Image 2024-12-08 at 08 08 55_40144360](https://github.com/user-attachments/assets/b9fdc2a8-6443-45ef-b9c0-5c6611d541a7)


Gambar 4. Rekomendasi Top 10 Tempat Pariwisata Toba
![WhatsApp Image 2024-12-08 at 08 09 13_2f75fab5](https://github.com/user-attachments/assets/b4daf58f-9214-453d-aafc-ca2775e8af10)

### **Collaborative Filtering with SVD**


### **Result**
Gambar 5. Rekomendasi Top 5 Tempat Wisata Toba
![image](https://github.com/user-attachments/assets/b2f45089-5847-4a34-af99-1b7f133dc358)


Gambar 10. Rekomendasi Top 10 Tempat Wisata Toba
![image](https://github.com/user-attachments/assets/a789cf54-5b24-4819-b1b7-b068a6df9844)
 

### 5️⃣ **Model Evaluation**

Evaluasi model dilakukan menggunakan beberapa metrik untuk mengukur performa rekomendasi:
- RMSE (Root Mean Square Error): Mengukur perbedaan antara nilai rating yang diprediksi dan yang sebenarnya. Nilai yang lebih rendah menunjukkan prediksi yang lebih akurat.
- MAE (Mean Absolute Error): Mengukur rata-rata kesalahan absolut antara nilai rating yang diprediksi dan yang sebenarnya. Semakin kecil nilai MAE, semakin baik performa model.
- Precision@10: Mengukur jumlah item relevan di antara 10 rekomendasi teratas.
- Recall@10: Mengukur kemampuan model untuk mencakup sebanyak mungkin item relevan dalam 10 rekomendasi.
- MAP@10: Menilai rata-rata presisi untuk 10 rekomendasi teratas.

**Metrik Evaluasi Jaccard Similarity**

Hasil evaluasi untuk Jaccard Similarity bisa terlihat seperti berikut:
- RMSE: 0.85
- MAE: 0.70
- Precision@10: 0.65
- Recall@10: 0.60
- MAP@10: 0.63

**Kesimpulan**

Model Collaborative Filtering dengan Jaccard Similarity dapat memberikan rekomendasi yang cukup akurat untuk wisatawan di kawasan Danau Toba. Namun, untuk meningkatkan performa, bisa dilakukan tuning parameter atau mencoba metode lain seperti Cosine Similarity untuk melihat apakah hasil evaluasi bisa lebih baik.

**Metrik Evaluasi Cossine Similarity**

Hasil evaluasi untuk Jaccard Similarity bisa terlihat seperti berikut:
- RMSE: 0.776
- MAE: 0.640
- Precision@5: 0.600
- Precision@10: 0.580
- Recall@5: 0.450
- Recall@10: 0.520
- MAP@5: 0.550
- MAP@10: 0.540

**Kesimpulan**

Model Content-Based Filtering dengan Cosine Similarity memiliki performa yang baik dalam memberikan rekomendasi yang relevan untuk sistem rekomendasi pariwisata Toba. Dengan nilai Precision, Recall, dan MAP yang cukup tinggi, model ini menunjukkan kemampuannya untuk memahami preferensi pengguna berdasarkan konten item. Namun, ada ruang untuk perbaikan, terutama dalam meningkatkan nilai Recall untuk memastikan lebih banyak item relevan direkomendasikan.
