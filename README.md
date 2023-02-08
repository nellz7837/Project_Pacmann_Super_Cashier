## Tentang Super Cashier
Self-service cashier sederhana dengan menggunakan bahasa pemrograman Python.

## Latar Belakang
Berawal dari keresahan seorang Andi tentang bisnis supermarket yang dijalaninya yang membutuhkan sistem self service cashier

## Requirements/Objective
- Membuat proses `tambah` barang belanjaan.
- Membuat proses `hapus` barang belanjaan.
- Membuat proses `edit nama` barang belanjaan.
- Membuat proses `edit jumlah` barang belanjaan. 
- Membuat proses `edit harga` barang belanjaan.
- Membuat proses `hitung total harga` barang belanjaan.
- Membuat proses `hitung diskon` barang belanjaan.
- Membuat proses `kosongkan barang` belanjaan.
- Mengecek barang belanjaan dengan `menampilkan seluruh barang belanjaan`.

## Flowchart
![simple flowchart](https://user-images.githubusercontent.com/117026628/217517730-93e60f48-224f-4307-bf30-2a270c0965e7.jpg)

## Generic Function
- `__init__`. Menginisiasi variable utama pada sebuah class. Dalam hal ini adalah variable `items` yang dinisiasi.

## Penjelasan Fungsi
Semua fungsi berikut terdapat di dalam class bernama `Transaction` pada file `main.py`:

## Method
- `add_item`. Menambahkan barang dengan format `add_item([item_name, qty, item_price])` ke dalam variable `items` di dalam class. Contoh: `add_item(['Ayam', 12, 15_000])`

- `update_item_name`. Mengganti nama barang saat ini dengan nama barang yang baru jika barang yang disebutkan tersedia dengan format `update_item_name(item_name, new_item_name)`. Contoh: `update_item_name('Ayam', 'Ayam Goreng')`

- `update_item_qty`. Mengganti jumlah pesanan barang jika barang yang disebutkan tersedia dengan format `update_item_qty(item_name, new_qty)`. Contoh: `update_item_qty('Ayam', 20)`.

- `update_item_price`. Mengganti harga per item barang jika barang yang disebutkan tersedia dengan format `update_item_price(item_name, new_price)`. Contoh `update_item_price('Ayam', 30_000)`

- `delete_item`. Menghapus barang berdasarkan nama di dalam `items` jika tersedia dengan format `delete_item(item_name)`. Contoh: `delete_item('Ayam')`

- `check_order`. Menampilkan semua barang yang telah ditambahkan beserta dengan total harga keseluruhan.

- `total_price_print`. Menampilkan seluruh barang beserta total harga tiap barang, discount, dan total setelah diskon.

- `reset_transaction`. Mengosongkan semua barang sekaligus yang telah ditambahkan.

- `calculate_total_price`. Menghitung harga total semua barang.

- `calculate_discount`. Menghitung jika total keseluruhan harga barang memenuhi syarat diskon. Syarat diskon adalah sebagai berikut:
	 - Jika di atas Rp 200.000 diskon sebesar 5%
   - Jika di atas Rp 300.000 diskon sebesar 8%
   - Jika di atas Rp 500.000 diskon sebesar 10%

## Modul
- `validate_add_item`. Validasi sebelum item ditambahkan. Meliputi format penulisan dan harga barang/qty tidak boleh negatif.
- `validate_update_item_name`. Validasi sebelum item diganti namanya. Meliputi format penulisan nama item baru dan nama item lama.
- `validate_update_item_qty`. Validasi sebelum qty item diupdate. Meliputi format penulisan dan qty tidak boleh negatif.
- `validate_update_item_price`. Validasi sebelum harga item diupdate. Meliputi format penulisan dan harga tidak boleh negatif.

## Demonstrasi Code
Membuat Customer1 dengan code `Customer1 = Transaction()`

### Test 1: add_item()
Customer ingin menambahkan dua item baru menggunakan method `add_item()`. Item yang ditambahkan adalah sebagai berikut:
- Nama Item: Ayam Goreng, Qty: 2, Harga: 20000
- Nama Item: Pasta Gigi, Qty: 3, Harga: 15000


![test 1](https://user-images.githubusercontent.com/117026628/217529044-c8d70b11-a8ed-43b0-aa4d-c54c27e0cec6.png)

### Test 2: delete_item()
Ternyata Customer salah membeli salah satu item dari belanjaan yang sudah ditambahkan, maka Customer menggukan method `delete_item()` untuk menghapus item. Item yang ingin dihapuskan adalah **Pasta Gigi**.


![test 2](https://user-images.githubusercontent.com/117026628/217529082-a881e664-05a0-4b60-89fd-804a8bb91749.png)
![test 2 1](https://user-images.githubusercontent.com/117026628/217530063-b39729da-ff19-459a-97b2-dafcb7972481.png)

### Test 3: reset_transaction()
Ternyata setelah dipikir-pikir, Customer salah memasukkan item yang ingin dibelanjakan! Daripada menghapusnya satu - satu, maka Customer cukup menggunakan method `reset_transaction()` untuk menghapus semua item yang sudah ditambahkan.


![test 3](https://user-images.githubusercontent.com/117026628/217530358-c38e8ee8-204c-43e5-8d9d-50002d7036c3.png)

### Test 4: total_price_print()
Setelah Customer selesai berbelanja, akan menghitung total belanja yang harus dibayarkan menggunakan method `total_price_print()`. Sebelum mengeluarkan output total belanja akan menampilkan item - item yang dibeli. Item yang ditambahkan adalah sebagai berikut:
- Nama Item: Ayam Goreng, Qty: 2, Harga: 20000


![test 4](https://user-images.githubusercontent.com/117026628/217533999-04e745fc-6eb6-4346-8139-12380ab639ca.png)


## Kesimpulan
Super cashier adalah program sederhana yang membantu penjual untuk menjual produknya secara efektif dan efisien.
