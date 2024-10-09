
# STUDI KASUS - 4:

## Soal: Volume Suara Ponsel

Tini baru saja membeli ponsel baru dan ingin mengatur volume suara dengan baik. Namun, volume suara pada ponsel tersebut hanya bisa diatur pada rentang 0 hingga 100. Tini ingin memastikan bahwa volume tidak pernah lebih tinggi dari 100 atau lebih rendah dari 0 saat dia menaikkan atau menurunkan volume.

### Instruksi:
Buatlah kelas `Phone` dengan properti `volume` (private). Buat metode untuk menaikkan dan menurunkan volume, dengan validasi agar volume hanya berada di antara 0 hingga 100.

### Hint Kode (Jangan diubah ya!):
```kotlin
class Phone(private var volume: Int) {

    // Fungsi untuk menaikkan volume
    fun increaseVolume(amount: Int) {
        // ...
    }

    // Fungsi untuk menurunkan volume
    fun decreaseVolume(amount: Int) {
        // ...
    }

    // Fungsi untuk mendapatkan volume saat ini
    fun getVolume(): Int {
        // ...
    }
}

fun main() {
    val myPhone = Phone(50)  // Volume awal 50
    
    // Tampilkan volume awal
    // ...

    // Naikkan volume sebesar 30
    // ...

    // Tampilkan volume setelah naik
    // ...

    // Turunkan volume sebesar 70
    // ...

    // Tampilkan volume setelah turun
    // ...

    // Coba naikkan volume melewati batas maksimum
    // ...

    // Tampilkan volume akhir
    // ...
}
```
