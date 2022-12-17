# Airlines Customer Satisfaction and Business Planning
Customer satisfied or dissatisfied analysis and recommendation

## Summary:
Merupakan final project pertama saya tentang Customer Classification pada Airlines Customer Satisfaction and Business Planning menggunakan Random Forest.

## Introduction:
Random Forest adalah kumpulan dari decision tree atau pohon keputusan. Algoritma ini merupakan kombinasi masing-masing dari decision tree yang kemudian digabungkan menjadi satu model. Biasanya, random forest dipakai untuk masalah regresi dan klasifikasi dengan kumpulan data yang berukuran besar. (dikutip dari : https://algorit.ma/blog/cara-kerja-algoritma-random-forest-2022/)

## Challenges : 
Customer satisfied or dissatisfied analysis and recommendation

## Data Analysis:
a.	Data Understanding
Source Dataset : https://www.kaggle.com/datasets/sjleshrac/airlines-customer-satisfaction
Dataset terdiri dari 23 kolom, 129880 baris, terdapat 393 missing value, 0 duplicated value

b.	Visualisasi Data 
-	Perbandingan satisfication, class dan gender
<img width="412" alt="image" src="https://user-images.githubusercontent.com/112957682/208232059-793afc3f-9e54-4ab0-9c28-f6ee25900c4e.png">

dari perbandingan variabel diatas dapat dilihat bahwa Female memiliki tingkat satisfaction lebih tinggi dari Male pada semua Class

-	Perbandingan variabel satisfaction, Type of Travel dan Gender
<img width="386" alt="image" src="https://user-images.githubusercontent.com/112957682/208232073-4dee677b-eab8-4b85-b93f-5e32cdd3abdb.png">

dari perbandingan variabel Type of Travel untuk Personal Travel Female memiliki tingkat satisfaction jauh lebih tinggi dari pada Male. dan untuk Business Travel Male memiliki tingkat satisfaction sedikit lebih tinggi daripada Female.

-	Perbandingan variabel satisfaction, Customer Type dan Gender
<img width="386" alt="image" src="https://user-images.githubusercontent.com/112957682/208232080-0280a5d7-e183-42c7-89f4-34faef953023.png">
 
dari perbandingan Customer Type untuk Loyal Customer Female memiliki tingkat satisfaction lebih tinggi daripada Male. dan untuk Disloyal Customer Male memiliki tingkat satisfaction lebih tinggi daripada Female

-	Perbandingan Variabel Delay Lengths (Arrival Dan Departure Delay in Minutes), Flight Distance
<img width="344" alt="image" src="https://user-images.githubusercontent.com/112957682/208232086-f7a2fa64-333f-492b-835e-e9244662f9fa.png">

<img width="395" alt="image" src="https://user-images.githubusercontent.com/112957682/208232090-d5d47ecb-881d-4794-b560-3692fb0ab82d.png">

<img width="360" alt="image" src="https://user-images.githubusercontent.com/112957682/208232095-b8f67f9c-daa3-4ce3-8d92-ff1810ef873a.png">

tingkat satisfaction sepertinya semakin menurun sebanding dengan lama Delay

-	Rasio orang yg satisfied dan dissatisfied
<img width="468" alt="image" src="https://user-images.githubusercontent.com/112957682/208232110-39ab090d-feea-45ca-9ae9-13cff93cfb25.png">

satisfied 54.7% dan dissatisfied 45.3%

-	Rasio Female dan Male yg satisfied dan dissatisfied
<img width="415" alt="image" src="https://user-images.githubusercontent.com/112957682/208232123-0275ae07-99c2-4f3c-abc3-0a5d11c969e8.png">

pada Satisfaction = 1(satisfied) Female lebih banyak daripada Male. dan pada Satisfaction = 0(dissatisfied) Male lebih banyak daripada Female

-	Heatmap Correlation
 <img width="468" alt="image" src="https://user-images.githubusercontent.com/112957682/208232135-b726def3-f42e-4623-b598-6344476607c0.png">

dari correlation heatmap diatas dapat dilihat Arrival Delay in Minutes dan Departure Delay in Minure memiliki korelasi yg kuat untuk menentukan Satisfaction

## Modelling
Modelling – Random Forest
<img width="468" alt="image" src="https://user-images.githubusercontent.com/112957682/208232149-e85ca11e-68c7-4568-a204-ce43836b3c74.png">

hasil analisis:
1.	True Positif = 16813 yg berarti diprediksi puas/satisfied dan benar satisfied sebanyak 16813.
2.	True Negative = 14268 yg berarti diprediksi tidak puas ternyata tidak puas sebanyak 14268.
3.	False Positive = 464 yg berarti diprediksi puas ternyata tidak puas sebanyak 464.
4.	False Negative = 827 yg berarti diprediksi tidak puas dan ternyata tidak puas sebanyak 827.

kita juga temukan:
1.	Accuracy = 96%. yg berarti perbandingan TP dan TN terhadap semua data tingkat akurasinya sebanyak 96%.
2.	Precision = 97% yg berarti diantara semua customer yg diprediksi puas ternyata yg sesungguhnya puas sebanyak 97%.
3.	Recall = 95% yg berarti diantara semua customer yg diprediksi puas yg berhasil diprediksi puas sebanyak 95%.

Kita ingin memprediksi kepuasan/satisfied customer untuk rencana bisnis kedepannya. Dari hasil diatas ingin menghilangkan False Positive, yaitu kita prediksi satisfied ternyata dissatisfied.

## Conclusion 

-	untuk semua jenis class (Eco, Business, Eco Pluss) Female memiliki tingkat satisfaction lebih tinggi dari Male. tapi pada class business perbedaan Satisfaction female dan Male hanya selisih sedikit saja.
-	untuk Type of Travel (Personal Travel dan Business Travel), pada Personal Travel Female memiliki tingkat satisfaction jauh lebih tinggi dari pada Male. dan untuk Business Travel Male memiliki tingkat satisfaction sedikit lebih tinggi daripada Female.
-	untuk Customer Type (Loyal Customer) Female memiliki tingkat satisfaction lebih tinggi daripada Male. dan untuk Disloyal Customer Male memiliki tingkat satisfaction lebih tinggi daripada Female.
-	tingkat satisfaction sepertinya semakin menurun sebanding dengan lamanya Delay(Departure maupun Arrival)
-	Female memiliki jumlah satisfied lebih banyak dibanding Male, dan sebaliknya Male memiliki jumlah Dissatisfied lebih banyak

## Recommendation

1.	Tingkatkan service untuk Male pada jenis Class Eco dan Eco Plus. misal promo yg menarik untuk tgl tertentu
2.	Tingkatkan service untuk Female pada jenis Class Business. misal promo yg menarik
3.	Tingkatkan service untuk Male pada Personal Travel, dan untuk Female pada Business Travel. misal promo yg menarik
4.	Tingkatkan pelayanan service secara keseluruhan untuk meminimalisir sekecil mungkin Delay baik departure maupun arrival.
5.	secara keseluruhan minimal harus mempertahankan satisfied Female dan harus meningkatkan service untuk Male supaya satisfied Male bisa lebih meningkat



