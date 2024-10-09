
# Tutorial Penggunaan Visibility Modifier `public` di Kotlin

Di Kotlin, **`public`** adalah visibility modifier default, artinya jika Anda tidak menentukan modifier pada anggota kelas (properti atau metode), maka secara otomatis akan menjadi `public`. Anggota `public` dapat diakses dari mana saja, termasuk dari luar kelas.

## Contoh Penggunaan `public`

Kita akan membuat kelas **`Animal`** yang memiliki properti `public` seperti `name`, `age`, `weight`, dan `isMammal`, serta cara mengakses properti-properti tersebut dari luar kelas.

### 1. Membuat Kelas dengan Properti `public`

Berikut ini adalah contoh kelas `Animal` dengan beberapa properti `public`.

```kotlin
class Animal(
    val name: String,  // Public by default
    val age: Int,      // Public by default
    val weight: Double // Public by default
) {
    val isMammal: Boolean = true // Public by default
}
```

Dalam contoh ini, `name`, `age`, `weight`, dan `isMammal` semuanya bersifat `public`, karena tidak ada visibility modifier lain yang ditetapkan. Secara default, mereka akan bisa diakses dari mana saja.

### 2. Mengakses Properti `public` dari Luar Kelas

Anda dapat membuat objek dari kelas `Animal` dan mengakses properti `public`-nya dari luar kelas seperti berikut:

```kotlin
fun main() {
    // Membuat objek Animal
    val lion = Animal("Lion", 5, 190.5)

    // Mengakses properti publik dari luar kelas
    println("Animal Name: ${lion.name}")     // Output: Lion
    println("Animal Age: ${lion.age}")       // Output: 5
    println("Animal Weight: ${lion.weight}") // Output: 190.5
    println("Is Mammal: ${lion.isMammal}")   // Output: true
}
```

Di sini, kita bisa mengakses properti `name`, `age`, `weight`, dan `isMammal` dari objek `lion`, karena semuanya memiliki visibility `public` secara default.

### 3. Mencoba Modifikasi Properti `public`

Satu hal yang perlu diperhatikan, properti `val` hanya bisa dibaca (read-only), jadi kita tidak bisa mengubah nilainya setelah objek dibuat. Jika Anda ingin properti bisa dimodifikasi, Anda bisa menggunakan `var` sebagai gantinya.

Contoh penggunaan `var` untuk properti `public`:

```kotlin
class Animal(
    var name: String,  // Mutable property (can be changed)
    var age: Int,      // Mutable property (can be changed)
    var weight: Double // Mutable property (can be changed)
) {
    var isMammal: Boolean = true
}

fun main() {
    // Membuat objek Animal
    val elephant = Animal("Elephant", 10, 500.0)

    // Mengakses dan memodifikasi properti publik
    println("Animal Name: ${elephant.name}") // Output: Elephant
    elephant.name = "Big Elephant"           // Modifying the name
    println("Updated Name: ${elephant.name}") // Output: Big Elephant
}
```

Dalam contoh ini, kita berhasil mengubah nilai properti `name` dari "Elephant" menjadi "Big Elephant" karena properti ini menggunakan `var`.

## Kesimpulan

Visibility modifier `public` memungkinkan anggota kelas diakses dari luar kelas tanpa batasan. Di Kotlin, `public` adalah default visibility modifier, jadi Anda tidak harus selalu menyatakannya secara eksplisit. Properti atau metode `public` dapat digunakan dan dimodifikasi sesuai kebutuhan, terutama jika properti tersebut ditetapkan sebagai `var`.

