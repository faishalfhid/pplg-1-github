
# STUDI KASUS - 3:

## Soal: Tabungan Arman

Arman adalah seorang siswa yang sedang menabung untuk membeli sepeda. Dia memiliki saldo awal sebesar Rp500.000 di celengannya. Arman hanya bisa menambah uang ke dalam celengannya, tetapi tidak bisa mengambil uang secara langsung dari sana. Setiap kali dia menambah uang, dia ingin mengetahui jumlah total uang yang ada di celengannya.

### Instruksi: 
Buatlah kelas `Savings` dengan properti `balance` (private). Buat metode untuk menambahkan uang ke dalam celengan, dan metode untuk melihat jumlah saldo saat ini.

### Hint Kode (Jangan diubah ya!):
```kotlin
class Savings(private var balance: Int) {

    // Fungsi untuk menambahkan uang
    fun addMoney(amount: Int) {
        // ...
    }

    // Fungsi untuk melihat saldo saat ini
    fun getBalance(): Int {
        // ...
    }
}

fun main() {
    val armanSavings = Savings(500000)  // Saldo awal Rp500.000

    // Arman menambah uang Rp100.000
    // ...

    // Tampilkan saldo saat ini
    // ...

    // Arman menambah uang Rp50.000
    // ...

    // Tampilkan saldo akhir
    // ...
}
```
