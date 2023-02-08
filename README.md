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
----cari dulu gambar flowchartnya---

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
  **Output:**

### Test 2: delete_item()
Ternyata Customer salah membeli salah satu item dari belanjaan yang sudah ditambahkan, maka Customer menggukan method `delete_item()` untuk menghapus item. Item yang ingin dihapuskan adalah **Pasta Gigi**.
 **Output:**

### Test 3: reset_transaction()
Ternyata setelah dipikir-pikir, Customer salah memasukkan item yang ingin dibelanjakan! Daripada menghapusnya satu - satu, maka Customer cukup menggunakan method `reset_transaction()` untuk menghapus semua item yang sudah ditambahkan.
 **Output:**


### Test 4: total_price_print()
Setelah Customer selesai berbelanja, akan menghitung total belanja yang harus dibayarkan menggunakan method `total_price_print()`. Sebelum mengeluarkan output total belanja akan menampilkan item - item yang dibeli. Item yang ditambahkan adalah sebagai berikut:
- Nama Item: Ayam Goreng, Qty: 2, Harga: 20000
- Nama Item: Pasta Gigi, Qty: 3, Harga: 15000
  **Output:**

### Test 5: update_item_name()
Item yang ditambahkan adalah sebagai berikut:
- Nama Item: Ayam Goreng, Qty: 2, Harga: 20000
Customer ingin mengganti nama **Ayam Goreng** yang terlanjur ditambahkan menggunakan metode `update_item_name()` sehingga nama item tersebut menjadi **Ayam Goreng Balado**
  **Output:**

### Test 6: update_item_qty()
Customer ingin mengganti Quantity dari **Ayam Goreng Balado** yang sebelumnya 2 buah menjadi 10 buah dengan metode `update_item_qty()`
  **Output:**

### Test 7: update_item_price()
Customer ingin mengganti harga per item dari **Ayam Goreng Balado** yang sebelumnya 20000 menjadi 25000 per item-nya dengan metode `update_item_price()`.
  **Output**:


## Kesimpulan
Super cashier adalah program sederhana yang membantu penjual untuk menjual produknya secara efektif dan efisien.
