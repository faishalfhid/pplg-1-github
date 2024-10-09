
# Tutorial Penggunaan Visibility Modifier `private` di Kotlin

Modifier `private` membatasi akses suatu properti atau fungsi sehingga hanya dapat diakses dari dalam kelas tempat properti atau fungsi tersebut dideklarasikan. Anggota yang diberi modifier `private` tidak bisa diakses dari luar kelasnya.

## Contoh Penggunaan `private`

Mari kita terapkan modifier `private` pada kelas **`Animal`** dan lihat bagaimana cara mengakses properti `private` dengan menambahkan getter dan setter secara manual.

### 1. Membuat Kelas dengan Properti `private`

Berikut adalah contoh kelas **`Animal`** di mana semua propertinya diubah menjadi `private`:

```kotlin
class Animal(private val name: String, private var age: Int) {
    // Tidak ada cara langsung untuk mengakses name dan age dari luar kelas ini
}

fun main() {
    val myPet = Animal("Kucing", 2)

    // Akan menghasilkan error karena properti 'name' bersifat private
    println("Nama: ${myPet.name}")  // Error: Cannot access 'name': it is private in 'Animal'
}
```

Pada contoh di atas, kita mencoba mengakses properti `name` dari objek `myPet`. Namun, karena properti `name` memiliki akses `private`, kode ini akan menghasilkan error: **"Cannot access 'name': it is private in 'Animal'"**.

### 2. Menggunakan Getter dan Setter untuk Mengakses Properti `private`

Untuk mengakses properti `private` dari luar kelas, kita harus membuat metode getter dan setter secara manual.

Berikut ini adalah contoh penambahan getter dan setter untuk properti `name` dan `age`:

```kotlin
class Animal(private var name: String, private var age: Int) {

    // Getter untuk name
    fun getName(): String {
        return name
    }

    // Setter untuk name
    fun setName(newName: String) {
        name = newName
    }

    // Getter untuk age
    fun getAge(): Int {
        return age
    }

    // Setter untuk age
    fun setAge(newAge: Int) {
        age = newAge
    }
}

fun main() {
    val myPet = Animal("Kucing", 2)

    // Menggunakan getter untuk mendapatkan nilai 'name'
    println("Nama hewan: ${myPet.getName()}") // Output: Kucing

    // Menggunakan setter untuk mengubah nilai 'name'
    myPet.setName("Banteng")
    println("Nama hewan setelah diubah: ${myPet.getName()}") // Output: Banteng

    // Menggunakan getter untuk mendapatkan nilai 'age'
    println("Umur hewan: ${myPet.getAge()}") // Output: 2

    // Menggunakan setter untuk mengubah nilai 'age'
    myPet.setAge(3)
    println("Umur hewan setelah diubah: ${myPet.getAge()}") // Output: 3
}
```

### 3. Penjelasan

- **Getter:** Digunakan untuk mengambil (membaca) nilai dari properti `private`.
- **Setter:** Digunakan untuk mengubah (menulis) nilai dari properti `private`.
- Kotlin secara otomatis menghasilkan getter dan setter untuk properti `public`, tetapi untuk `private`, kita harus membuatnya sendiri.

## Kesimpulan

Dengan menggunakan visibility modifier `private`, kita bisa membatasi akses ke properti dan fungsi dari luar kelas. Ini memberikan kontrol lebih besar atas bagaimana data diproses di dalam kelas. Namun, jika kita ingin tetap dapat mengakses atau mengubah nilai properti tersebut dari luar kelas, kita harus membuat getter dan setter secara manual.
