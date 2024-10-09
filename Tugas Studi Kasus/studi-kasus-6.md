
# Studi Kasus - 6: Produk di Toko Online

## Soal: Produk di Toko Online
Sebuah toko online sedang menjual produk berupa laptop dengan harga **Rp15.000.000**. Pemilik toko ingin memastikan bahwa harga produk tidak boleh diubah menjadi nilai negatif. Setiap kali harga produk diubah, pemilik toko ingin melihat harganya secara real-time. Anda diminta untuk membantu pemilik toko menjaga integritas data harga produk.

## Instruksi
Buat kelas `Product` dengan properti `name` (public) dan `price` (private). Buat metode untuk mendapatkan dan mengubah harga produk dengan validasi agar harga tidak boleh negatif.

## Hint Kode (Jangan diubah ya!)
```kotlin
class Product(val name: String, private var price: Double) {

    // Fungsi untuk mendapatkan harga produk
    ???

    // Fungsi untuk mengatur harga dengan validasi
    ???
}

fun main() {
    val product = Product("Laptop", 15000000.0)
    
    // Pemilik toko ingin melihat harga produk saat ini
    
    // Pemilik toko mencoba mengubah harga menjadi nilai yang tidak valid (contoh: -500000.0)
    
    // Tampilkan harga produk setelah perubahan tidak valid
    
    // Pemilik toko memperbarui harga produk menjadi nilai yang valid (contoh: 12000000.0)
    
    // Tampilkan harga produk setelah perubahan valid
}
```
