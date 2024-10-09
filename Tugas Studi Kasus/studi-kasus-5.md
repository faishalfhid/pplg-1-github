
# Studi Kasus - 5: Penerbitan Buku Baru

## Soal: Penerbitan Buku Baru
Sebuah penerbit sedang mencetak buku baru dengan judul **"Pemrograman Kotlin"**. Mereka ingin memastikan bahwa jumlah halaman buku tersebut lebih dari 0 sebelum buku dicetak. Jika ada kesalahan dalam memasukkan jumlah halaman, penerbit harus bisa mengoreksinya sebelum proses produksi dimulai.

## Instruksi
Buat kelas `Book` dengan properti `title` (public) dan `pages` (private). Buat metode untuk mendapatkan dan mengubah jumlah halaman dengan validasi agar nilai `pages` hanya bisa diubah jika lebih dari 0.

## Kode Awal (Hint)
```kotlin
class Book(val title: String, private var pages: Int) {

    // Fungsi untuk mendapatkan jumlah halaman
    ???

    // Fungsi untuk mengatur jumlah halaman dengan validasi
    ???
}

fun main() {
    val book = Book("Pemrograman Kotlin", 300)
    
    // Penerbit ingin melihat jumlah halaman awal
    
    // Penerbit mencoba mengubah jumlah halaman menjadi nilai yang tidak valid (contoh: -10)
    
    // Tampilkan jumlah halaman setelah perubahan tidak valid
    
    // Penerbit memperbarui jumlah halaman menjadi nilai yang valid (contoh: 350)
    
    // Tampilkan jumlah halaman setelah perubahan valid
}
```

## Solusi yang Diharapkan
Kelas `Book` harus memiliki metode untuk mendapatkan jumlah halaman serta mengubahnya dengan validasi sehingga nilai halaman harus lebih dari 0. 

### Implementasi Kode
```kotlin
class Book(val title: String, private var pages: Int) {

    // Fungsi untuk mendapatkan jumlah halaman
    fun getPages(): Int {
        return pages
    }

    // Fungsi untuk mengatur jumlah halaman dengan validasi
    fun setPages(newPages: Int) {
        if (newPages > 0) {
            pages = newPages
        } else {
            println("Jumlah halaman harus lebih dari 0.")
        }
    }
}

fun main() {
    val book = Book("Pemrograman Kotlin", 300)
    
    // Penerbit ingin melihat jumlah halaman awal
    println("Jumlah halaman awal: " + book.getPages())
    
    // Penerbit mencoba mengubah jumlah halaman menjadi nilai yang tidak valid (contoh: -10)
    book.setPages(-10)
    
    // Tampilkan jumlah halaman setelah perubahan tidak valid
    println("Jumlah halaman setelah perubahan tidak valid: " + book.getPages())
    
    // Penerbit memperbarui jumlah halaman menjadi nilai yang valid (contoh: 350)
    book.setPages(350)
    
    // Tampilkan jumlah halaman setelah perubahan valid
    println("Jumlah halaman setelah perubahan valid: " + book.getPages())
}
```

### Output yang Diharapkan:
```
Jumlah halaman awal: 300
Jumlah halaman harus lebih dari 0.
Jumlah halaman setelah perubahan tidak valid: 300
Jumlah halaman setelah perubahan valid: 350
```
