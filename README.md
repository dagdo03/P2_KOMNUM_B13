Kelompok 13 :
1. Tengku Fredly Reinaldo (5025201198)
2. Ihsan Widagdo (5025211231)
3. Lihardo Marson Purba (5025211238)


METODE INTEGRASI TRAPEZOIDAL VS METODE INTEGRASI ROMBERG

PENGANTAR 

Trapezoidal
Sama seperti Namanya, metode ini menggunakan rumus trapezium dimana dalam implementasinya kita menjumlahkan luas trapezium yang berasal dari pembagian bidang yang dibentuk suatu garis fungsi f(x) dan garis y =0. Dimana diilustrasikan sebagai berikut : 

![image](https://user-images.githubusercontent.com/95538168/208995166-a75d10e5-a4e3-4bb1-808c-68f68dacbab5.png)

 
Pada gambar diatas apabila diambil satu ruas trapezium maka kita akan melihat jelas bahwa setiap ruasnya itu merupakan bidang trapezium yang ditunjukkan gambar dibawah ini:  

![image](https://user-images.githubusercontent.com/95538168/208995211-8879084b-1091-4269-9cec-1ea588e02ec1.png)

Ole karena itu, Untuk mendapat integral dari fungsi tersebut kita perlu menjumlahkan semua luas dari ruas – ruas yang dibagi dari bidang yang terbentuk oleh garis f(x) dan y=0.


Jika dibuat secara ilmiah maka rumus yang digunakan adalah sebagai berikut :

![image](https://user-images.githubusercontent.com/95538168/208995273-b6126b5a-7c66-4675-bf72-a82802bfb875.png)

 
	ROMBERG
Ide utama dalam metode integrasi yang satu ini adalah pengurangan atau penghilangan eror dari setiap iterasi yang diterapkan. Pada metode ini kita menggunakan Richardson Exptrapolation untuk mengurangi jumlah eror dari setiap iterasi yang dilakukan. 
Jika kita menerapkan Richardson Exptrapolation pada metode integrasi Trapezoidal maka jika diilustrasikan, kita perlu mengevaluasi setiap nilai dari luas setiap trapezium yang dibagi dari bidang yang terbentuk oleh garis f(x) dan y =0. 

![image](https://user-images.githubusercontent.com/95538168/208995298-b1676c96-5409-4c70-a036-fd1770b10266.png)

 
Dengan menggunakan ilustrasi yang sama, kita bisa melihat bahwa metode ini mengevaluasi setiap nilai yang terbentuk oleh setiap ruas trapezium yang terlihat pada gambar diatas. Dengan mengevaluasi setiap nilai dari pembagian ruas trapezium maka akan didapat hasil yang sangat akurat dimana kita menggunakan Richardson Extrapolation untuk mengevaluasinya.
Untuk persamaannya akan menjadi :
R_1,1=h/2 [f(a)+f(b)]
R_2,1=h/4 [f(a)+f(a+h/2  )+f(b)]
R_3,1=h/8 [f(a)+f(a+h/4  )+f(a+h/2  )+f(b)]

R_2,2=R_1,1+1/3 [R_2,1-R_1,1 ]
R_3,2=R_3,1+1/3 [R_3,1-R_2,1 ]


R_3,3=R_3,2+1/15 [R_3,2-R_2,2 ]


SECARA UMUM :
R_(k,j)=R_(k,j-1)+1/(4^(j-1)-1) [R_(k,j-1)-R_(k-1,j-1) ]

NOTE : 
Semakin besar nilai j maka semakin besar pula tingkat akurasi dari nilai yang diperoleh dari perhitungan yang dilakukan.

KESIMPULAN : 
Jika pada metode trapezoidal kita dituntut untuk menggunakan banyak iterasi(banyak pembagian trapezium) untuk mengeleminasi nilai – nilai yang tidak akurat seperti pada gambar dibawah.

![image](https://user-images.githubusercontent.com/95538168/208995378-b3ffe3ad-59dc-44bb-8e44-6fa6d927a784.png)

 
Tetapi, dengan metode Romberg dengan iterasi yang sedikit kita bisa mendapat hasil yang lebih akurat karena kita mengevaluasi setiap nilai ruas yang terbentuk oleh trapezium tersebut. Disisi lain, Romberg memiliki kelemahan karena jika kita ingin mendapat nilai yang akurat maka kita perlu melakukan swipe banyak dengan tujuan mengurangi nilai erornya. Tetapi jika kita ingin melakukan banyak swipe kita juga perlu melakukan banyak perhitungan untuk melakukan banyak swipe juga.

