
# Studi Kasus: Mobil Balap Jack

Jack adalah seorang pembalap yang ingin menguji mobil balap barunya. Dia ingin memastikan bahwa mobilnya tidak melaju lebih dari 200 km/jam demi alasan keamanan. Saat ini, mobil tersebut berjalan dengan kecepatan 50 km/jam, dan Jack berencana untuk menambah kecepatan secara bertahap selama uji coba. Bantulah Jack mengatur kecepatan mobilnya agar tidak melebihi batas yang sudah ditentukan.

## Instruksi

- Buat kelas `Car` dengan properti `brand` (public) dan `speed` (private).
- Buat metode untuk mendapatkan dan menambah kecepatan dengan validasi agar kecepatan tidak boleh melebihi 200 km/jam.

## Hint Kode (Jangan diubah ya!)

```kotlin
class Car(val brand: String, private var speed: Int) {

    // Fungsi untuk mendapatkan nilai speed
    fun getSpeed(): Int {
        return speed
    }

    // Fungsi untuk menambah kecepatan
    fun increaseSpeed(increment: Int) {
        if (speed + increment > 200) {
            speed = 200
        } else {
            speed += increment
        }
    }
}

fun main() {
    val car = Car("Toyota", 50)

    // Jack memulai uji coba mobil balap dengan menampilkan kecepatan awal
    println("Kecepatan awal: ${car.getSpeed()} km/jam")

    // Jack menambah kecepatan mobil sebanyak 100 km/h.
    car.increaseSpeed(100)

    // Tampilkan kecepatan mobil setelah penambahan
    println("Kecepatan setelah ditambah: ${car.getSpeed()} km/jam")
    
    // Jack menambah lagi kecepatan sebanyak 100 km/h, seharusnya kecepatan tidak melebihi 200 km/jam
    car.increaseSpeed(100)

    // Tampilkan kecepatan mobil setelah penambahan
    println("Kecepatan setelah penambahan kedua: ${car.getSpeed()} km/jam")
}
```

## Penjelasan

1. **Kelas `Car`:** Kelas ini memiliki properti `brand` (public) yang menunjukkan merek mobil dan `speed` (private) yang menyimpan kecepatan mobil.
   
2. **Fungsi `getSpeed`:** Fungsi ini digunakan untuk mengembalikan nilai kecepatan mobil saat ini.

3. **Fungsi `increaseSpeed`:** Fungsi ini digunakan untuk menambah kecepatan mobil. Fungsi ini juga memastikan bahwa kecepatan mobil tidak akan melebihi 200 km/jam. Jika penambahan kecepatan menyebabkan nilai kecepatan melebihi 200, maka kecepatan akan disetel ke 200.

4. **Main Function:**
   - **Langkah 1:** Jack memulai dengan kecepatan awal 50 km/jam.
   - **Langkah 2:** Jack menambah kecepatan sebesar 100 km/jam. Setelah itu, kecepatan menjadi 150 km/jam.
   - **Langkah 3:** Jack menambah lagi 100 km/jam, namun kecepatan mobil dibatasi menjadi 200 km/jam demi keamanan.

## Kesimpulan

Pada studi kasus ini, kita belajar bagaimana membatasi nilai properti privat dalam sebuah kelas menggunakan fungsi validasi di Kotlin. Dalam kasus Jack, kecepatan mobil tidak boleh melebihi 200 km/jam, sehingga kita mengontrol perubahan nilai properti `speed` menggunakan metode `increaseSpeed`.
