
# CONTOH LATIHAN: 
## STUDI KASUS - PENGATURAN SUHU AC:

Budi baru saja memasang AC di kamarnya dan ingin mengatur suhu ruangan sesuai kebutuhan. Namun, suhu AC hanya bisa diatur dalam rentang 16 hingga 30 derajat Celcius. Setiap kali Budi mengubah suhu, ia ingin memastikan bahwa suhu tersebut tidak melampaui batas yang diperbolehkan.

### Instruksi: 
Buatlah kelas `Air Conditioner` dengan properti `temperature` (private). Buat metode untuk menaikkan dan menurunkan suhu dengan validasi agar suhu hanya berada di antara 16 hingga 30 derajat Celsius. Buat juga metode untuk melihat suhu saat ini.

### Hint Kode (Jangan diubah ya!):
```kotlin
class AirConditioner(private var temperature: Int) {
    // ...
}

fun main() {
    val ac = AirConditioner(25)  // Suhu awal 25 derajat
    
    // Tampilkan suhu awal
    // ...
    
    // Naikkan suhu sebesar 5 derajat
    // ...
    
    // Tampilkan suhu setelah naik
    // ...
    
    // Turunkan suhu sebesar 10 derajat
    // ...
    
    // Tampilkan suhu setelah turun
    // ...
    
    // Coba naikkan suhu melewati batas maksimum
    // ...
    
    // Tampilkan suhu akhir
    // ...
}
```

### JAWABAN:
```kotlin
class AirConditioner(private var temperature: Int) {

    // Fungsi untuk mendapatkan suhu saat ini
    fun getTemperature(): Int {
        return temperature
    }

    // Fungsi untuk menaikkan suhu dengan validasi
    fun increaseTemperature(amount: Int) {
        if (temperature + amount <= 30) {
            temperature += amount
        } else {
            println("Suhu tidak boleh lebih dari 30 derajat Celsius.")
        }
    }

    // Fungsi untuk menurunkan suhu dengan validasi
    fun decreaseTemperature(amount: Int) {
        if (temperature - amount >= 16) {
            temperature -= amount
        } else {
            println("Suhu tidak boleh kurang dari 16 derajat Celsius.")
        }
    }
}

fun main() {
    val ac = AirConditioner(25)  // Suhu awal 25 derajat
    
    // Tampilkan suhu awal
    println("Suhu awal: ${ac.getTemperature()} derajat Celsius")
    
    // Naikkan suhu sebesar 5 derajat
    ac.increaseTemperature(5)
    
    // Tampilkan suhu setelah naik
    println("Suhu setelah naik: ${ac.getTemperature()} derajat Celsius")
    
    // Turunkan suhu sebesar 10 derajat
    ac.decreaseTemperature(10)
    
    // Tampilkan suhu setelah turun
    println("Suhu setelah turun: ${ac.getTemperature()} derajat Celsius")
    
    // Coba naikkan suhu melewati batas maksimum
    ac.increaseTemperature(10)
    
    // Tampilkan suhu akhir
    println("Suhu akhir: ${ac.getTemperature()} derajat Celsius")
}
```

### PENJELASAN KODE:
Kode ini merupakan implementasi sederhana dari enkapsulasi dalam pemrograman, di mana akses ke properti `temperature` dibatasi. Class `Air Conditioner` memungkinkan pengguna untuk mengatur suhu dengan batasan tertentu (16-30 derajat Celcius), serta memvalidasi setiap perubahan suhu untuk memastikan nilai yang wajar.
