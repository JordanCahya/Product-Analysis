# Product-Analysis
Studi ini untuk menentukan dan menganalisa lebih lanjut 10 kategori produk yang dimiliki oleh perusahaan.

# Objektif yang akan dianalisa pada studi ini antara lain:
Perusahaan ingin mengetahui 10 kategori produk yang paling diminati/paling banyak diorder
Perusahaan ingin melihat total penjualan dari 10 kategori produk yang terbesar
Perusahaan menginginkan informasi pertumbuhan pemesanan produk dari 10 produk yang paling diminati

Analisa ini menggunakan 4 DataFrame dengan penjelasan kolom sebagai berikut:

1. olist_order_dataset

'order_id' (object) = pengidentifikasi unik pemesanan dari pesanan
'order_purchase_timestamp' (object) = Menunjukan timestamp dari pembelian
'order_approved_at' (object) = Menunjukan timestamp dari pembayaran yang terverifikasi

2. olist_order_items_dataset

'order_id' (object) = pengidentifikasi unik pemesanan
'order_item_id' (int) = jumlah barang yang dipesan
'product_id' (object) = pengidentifikasi unik produk
'price' (int) = harga barang
'freight_value' (int) = nilai angkutan barang

3. olist_products_dataset

'product_id' (object) = pengidentifikasi unik produk
'product_category_name' (object) = nama produk dalam bahasa portugis

# Eksplorasi dan pemrosesan data¶

Berikut merupakan langkah-langkah yang dilakukan untuk mengeksplorasi dan memproses data:

1. Mencari dan menangani missing value
2. Mencari duplikat data
3. Melakukan analisa perbedaan jumlah value unik dengan syntax len() pada olist_product_dataset DataFrame dan product_category_name_translation DataFrame
4. Melakukan merge olist_product_dataset DataFrame dengan product_category_name_translation DataFrame (left-join) untuk mengganti value di kolom product_category_name pada olist_product_dataset (bahasa portugis) menjadi bahasa inggris 
5. Melakukan merge pada olist_product_dataset, olist_order_items_dataset, dan olist_order_dataset

# Analisa dan kesimpulan

1. Perusahaan ingin mengetahui 10 kategori produk yang paling diminati/paling banyak diorder

Answer:
Furniture_decor menempati posisi pertama sebagai kategori produk yang paling diminati/paling banyak diorder.

2. Perusahaan ingin melihat total penjualan dari 10 kategori produk yang terbesar

Answer: 
computer_accessories menempati posisi pertama sebagai kategori produk yang memiliki total penjualan yang terbesar

3. Perusahaan menginginkan informasi pertumbuhan pemesanan produk dari 10 produk yang paling diminati

Dengan bantuan visualisasi menggunakan barplot, pertumbuhan kategori produk yang paling pesat terlihat pada kategori produk bed_bath_table.

# Konklusi

Setelah menganalisa ketiga objektif diatas, dapat diketahui bahwa kategori produk yang paling diminati/paling banyak diorder 
tidak selalu mendatangkan pendapatan yang paling besar. Dapat dilihat bahwa furniture_decor menempati pada posisi 1 sebagai produk yang paling diminati, 
namun menempati posisi ketiga pada total penjualan. 

Selain itu, produk bed_bath_table merupakan produk paling bagus performanya (pertumbuhan, total penjualan, dan merupakan produk yang paling diminati) 
jika dibandingkan dengan produk lain. Sedangkan, performa produk garden_tools perlu diperhatikan dikarenakan menurun secara signifikan dari 1399 
menjadi 993 (turun sebesar 29 persen). Perusahaan perlu mencari penyebab penurunan signifikan pada produk garden_tools.
