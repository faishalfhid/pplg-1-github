
# STUDI KASUS - 2:

## Soal: Nilai GPA (IPK) Mahasiswa

Pak Dedi adalah seorang dosen di Universitas Brawijaya. Dia sedang mengelola data mahasiswa, salah satunya adalah nilai GPA (Grade Point Average). GPA mahasiswa harus berada dalam rentang 0.0 hingga 4.0, dan Pak Dedi ingin memastikan tidak ada kesalahan dalam input data. Ia meminta bantuan untuk memeriksa dan memperbarui GPA mahasiswanya dengan tepat.

### Instruksi: 
Buat kelas `Student` dengan properti `name` (public) dan `gpa` (private). Buat metode untuk mengatur dan mendapatkan nilai gpa, serta validasi agar gpa hanya bisa diubah jika nilainya antara 0.0 hingga 4.0.

### Hint Kode (Jangan diubah ya!):
```kotlin
class Student(val name: String, private var gpa: Double) {

    // Fungsi untuk mendapatkan nilai gpa
    ???

    // Fungsi untuk mengatur nilai gpa dengan validasi
    ???
}

fun main() {
    val student = Student("Alice", 3.5)
    
    // Pak Dedi ingin melihat GPA Alice saat ini
    
    // Pak Dedi mencoba memasukkan nilai GPA yang tidak valid (contoh: 5.0)
    
    // Lihat apakah nilai GPA berubah setelah input tidak valid
    
    // Pak Dedi memperbarui GPA Alice ke nilai yang valid (contoh: 3.9)
    
    // Tampilkan GPA setelah perubahan
}
```
