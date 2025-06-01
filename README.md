# Laporan Praktikum: Exception Handling
# Pendahuluan
Exception handling adalah mekanisme dalam Java untuk menangani error atau kondisi exceptional yang terjadi saat program berjalan. Praktikum ini bertujuan untuk memahami konsep try-catch, throws, finally, dan custom exception.
# Analisis Percobaan
# Percobaan 1

Error: ArrayIndexOutOfBoundsException karena mengakses indeks ke-5 pada array berukuran 5.

Penanganan: Menambahkan blok try-catch untuk menangkap exception.

Output: "Terjadi pelanggaran memory"

Analisa: Kesalahan terjadi karena array hanya memiliki indeks dari 0 hingga 4. Dengan exception handling, program tidak berhenti secara paksa.

# Percobaan 2

Error: ArrayIndexOutOfBoundsException akibat perulangan while(i<4) melebihi panjang array.

Penanganan: Menambahkan try-catch di dalam loop dan me-reset nilai i ketika terjadi exception.

Output: Mengulang mencetak isi array karena i di-reset ke 0.

Analisa: Penanganan exception di dalam loop memungkinkan kontrol alur program saat terjadi kesalahan.

# Percobaan 3

Error: ArithmeticException karena pembagian dengan nol.

Penanganan: Menambahkan try-catch untuk menangani pembagian tersebut.

Output: "Ini menghandle error yang terjadi"

Analisa: Pembagian dengan nol adalah kesalahan umum yang harus ditangani agar program tidak crash.

# Percobaan 4

Error: Ada dua potensi error: pembagian dengan nol dan mengakses indeks array yang tidak ada.

Penanganan: Memisahkan pengecekan ke dalam try-catch dengan urutan yang tepat.

Output: "Terjadi Aritmatika error" karena urutan operasi dimulai dari pembagian terlebih dahulu.

Analisa: Urutan operasi dalam blok try mempengaruhi exception yang muncul terlebih dahulu.

# Percobaan 5

Error: ArithmeticException karena bil/0.

Penanganan: Menangani dengan try-catch, lalu menampilkan pesan error menggunakan getMessage() dan printStackTrace().

Output: Menampilkan detail lengkap dari exception.

Analisa: Metode printStackTrace() dan getMessage() berguna untuk debugging yang lebih detail.

# Percobaan 6

Error: Tidak ada error logis, tapi program melempar NullPointerException secara manual.

Penanganan: throw digunakan untuk melempar exception secara eksplisit.

Output: Menampilkan pesan error dari exception yang dilempar.

Analisa: Demonstrasi penggunaan throw untuk membuat error secara manual dan menanganinya dengan tepat.

# Percobaan 7

Error: Melempar exception baru dengan throw new Exception(...).

Penanganan: Tangkap dengan catch, lalu tampilkan informasi exception.

Output: Informasi dari getMessage(), toString(), dan printStackTrace().

Analisa: Memberikan gambaran detail mengenai isi dan struktur exception dalam Java.

# Percobaan 8

Error: ArithmeticException terjadi dalam methodB yang dideklarasikan melempar IOException.

Penanganan: Versi awal hanya melempar IOException, versi revisi menambahkan try-catch di main untuk menangani semua exception dan finally untuk mencetak pesan akhir.

Output: "Error di Method B", lalu "Ini selalu dicetak"

Analisa: Penggunaan finally memastikan ada bagian program yang selalu dijalankan walaupun terjadi error.

# Percobaan 9

Error: Method reverse() melempar exception jika string kosong.

Penanganan: Tangani exception menggunakan try-catch di method main.

Output: Menampilkan string terbalik jika tidak kosong, atau pesan error jika kosong.

Analisa: Validasi input sebelum pemrosesan sangat penting agar program tidak error di runtime.

# Percobaan 10

Error: Potensi IOException saat menulis/menutup file menggunakan RandomAccessFile.

Penanganan: Gunakan try-catch untuk menangkap IOException dan pastikan file ditutup.

Output: Menampilkan isi file "books.txt", jika tidak error.

Analisa: File I/O sangat rentan error, sehingga harus selalu dibungkus dalam blok try-catch.

# Percobaan 11

Error: Melempar exception buatan sendiri yang mewarisi Throwable.

Penanganan: Tangkap exception buatan (RangeErrorException) menggunakan catch.

Output: "Range error: Position 1"

Analisa: Programmer bisa membuat exception khusus untuk kebutuhan aplikasi tertentu.

# Percobaan 12

Error: Melempar exception buatan (MyException) jika input "amir".

Penanganan: Tangkap menggunakan catch dan tampilkan pesan.

Output:

Jika input "ali": tampil normal.

Jika input "amir": tampilkan pesan exception.

Analisa: Dengan membuat custom exception, program menjadi lebih ekspresif dan mudah dibaca.

# Kesimpulan

Java menyediakan mekanisme yang kuat untuk menangani error melalui exception handling.

Dengan try-catch, program tidak langsung berhenti saat terjadi kesalahan.

throw dan throws berguna untuk mendefinisikan dan melempar exception secara manual.

Penanganan exception penting untuk membuat program yang robust dan user-friendly.

# Saran
Selalu periksa operasi yang berpotensi gagal, seperti akses array, pembagian, dan I/O.

Gunakan finally untuk kode yang harus selalu dijalankan, misalnya menutup file atau koneksi.

Dokumentasikan exception yang mungkin terjadi untuk mempermudah debugging.
