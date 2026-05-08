# DATA-MINING.

# Klasifikasi Kualitas Wine Berdasarkan Karakteristik Kimiawi Menggunakan Machine Learning

## Deskripsi Project

Project ini membahas penerapan machine learning untuk memprediksi kualitas wine berdasarkan karakteristik kimiawi. Dataset yang digunakan terdiri dari data training dan data testing.

Data training digunakan untuk melatih dan mengevaluasi model karena memiliki kolom target `quality`. Sementara itu, data testing tidak memiliki kolom `quality`, sehingga nilai tersebut diprediksi menggunakan model terbaik yang diperoleh dari hasil evaluasi.

Permasalahan ini termasuk dalam kasus **classification** karena target `quality` diperlakukan sebagai kelas kualitas wine. Meskipun nilai quality berbentuk angka, nilai tersebut merepresentasikan kategori kualitas, bukan nilai numerik kontinu.

## Tujuan Project

Tujuan dari project ini adalah:

1. Memahami struktur dan karakteristik dataset Wine Quality.
2. Melakukan pengecekan missing value dan data duplikat.
3. Melakukan eksplorasi data untuk memahami distribusi target dan fitur.
4. Mengecek ketidakseimbangan kelas pada target `quality`.
5. Mengidentifikasi dan menangani outlier pada fitur numerik.
6. Melakukan preprocessing data sebelum pemodelan.
7. Membandingkan beberapa model klasifikasi.
8. Mengevaluasi performa model menggunakan accuracy, precision macro, recall macro, dan f1 macro.
9. Menentukan model terbaik berdasarkan hasil evaluasi.
10. Menggunakan model terbaik untuk memprediksi nilai `quality` pada data testing.
11. Menyimpan hasil prediksi dalam format CSV yang hanya berisi `Id` dan `Quality`.

## Dataset

Dataset memiliki beberapa fitur kimiawi wine, yaitu:

- `fixed acidity`
- `volatile acidity`
- `citric acid`
- `residual sugar`
- `chlorides`
- `free sulfur dioxide`
- `total sulfur dioxide`
- `density`
- `pH`
- `sulphates`
- `alcohol`

Selain fitur tersebut, data training memiliki kolom `quality` sebagai target. Kolom `Id` digunakan sebagai identitas data dan tidak digunakan sebagai fitur dalam pemodelan.

## Metode

Project ini menggunakan tahapan **CRISP-DM**, yaitu:

1. **Business Understanding**  
   Memahami tujuan project, yaitu memprediksi kualitas wine berdasarkan fitur kimiawi.

2. **Data Understanding**  
   Memahami struktur data, distribusi target, korelasi antar variabel, dan kemungkinan outlier.

3. **Data Preparation**  
   Melakukan pengecekan missing value, data duplikat, penanganan outlier menggunakan IQR capping, encoding target, dan pembagian data training-validasi.

4. **Modelling**  
   Membandingkan beberapa model klasifikasi menggunakan pipeline yang terdiri dari StandardScaler, SMOTE, dan model klasifikasi.

5. **Evaluation**  
   Mengevaluasi model menggunakan Accuracy, Precision Macro, Recall Macro, F1 Macro, classification report, dan confusion matrix.

6. **Deployment**  
   Menggunakan model terbaik untuk memprediksi data testing dan menyimpan hasil prediksi dalam file CSV.

## Model yang Digunakan

Beberapa model klasifikasi yang dibandingkan adalah:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- AdaBoost
- K-Nearest Neighbors
- Support Vector Machine
- Gaussian Naive Bayes
- XGBoost
- LightGBM

Model terbaik dipilih berdasarkan hasil evaluasi pada data validasi.

## Hasil Evaluasi

Berdasarkan hasil evaluasi, model terbaik yang diperoleh adalah **Random Forest**. Model ini menghasilkan nilai accuracy dan F1 Macro tertinggi dibandingkan model lainnya.

Random Forest kemudian digunakan sebagai model akhir untuk memprediksi nilai `quality` pada data testing.

## Feature Importance

Hasil feature importance menunjukkan bahwa beberapa fitur yang berpengaruh dalam prediksi kualitas wine antara lain:

- `volatile acidity`
- `sulphates`
- `alcohol`
- `citric acid`

Hal ini menunjukkan bahwa kualitas wine dipengaruhi oleh kombinasi beberapa karakteristik kimiawi.

## Output

Output akhir dari project ini adalah file CSV yang berisi dua kolom:

- `Id`
- `Quality`

Kolom `Id` digunakan sebagai identitas data testing, sedangkan kolom `Quality` berisi hasil prediksi kualitas wine.

## Kesimpulan

Project ini menunjukkan bahwa machine learning dapat digunakan untuk membantu memprediksi kualitas wine berdasarkan data kimiawi. Dengan membandingkan beberapa model klasifikasi, pemilihan model menjadi lebih objektif karena didasarkan pada hasil evaluasi.

Model Random Forest menjadi model terbaik dalam project ini dan digunakan untuk menghasilkan prediksi akhir pada data testing.
