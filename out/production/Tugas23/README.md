# 🎓 Program Kelulusan Siswa Modular (Java)

Proyek ini berisi program Java yang bertujuan untuk menentukan status kelulusan siswa berdasarkan nilai dan kehadiran, dengan penekanan kuat pada prinsip **modularitas** dan **refactoring** kode untuk meningkatkan keterbacaan, pemeliharaan, dan skalabilitas.

## ✨ Fitur Utama

* **Penentuan Status Kelulusan:** Menghitung status LULUS atau TIDAK LULUS untuk setiap siswa.
* **Kriteria yang Dapat Dikonfigurasi:** Kriteria kelulusan (nilai minimum dan kehadiran minimum) didefinisikan sebagai konstanta dan mudah diubah.
* **Desain Modular (OOP):** Menggunakan kelas-kelas terpisah untuk menangani data (`Siswa`), kriteria (`KriteriaKelulusan`), logika pemrosesan (`ValidatorKelulusan`), dan output.
* **Pure Function:** Logika validasi inti (`cekStatus`) diisolasi sebagai *pure function* (hanya bergantung pada input).
* **Laporan yang Terstruktur:** Menghasilkan laporan kelulusan yang jelas dengan status dan catatan.

## 🛠️ Refactoring yang Diterapkan

Kode ini merupakan hasil refactoring dari versi sebelumnya dan menerapkan beberapa teknik penting:

| Refactoring | Deskripsi |
| :--- | :--- |
| **Extract Class** | Membuat kelas `Siswa`, `StatusKelulusan`, dan `ValidatorKelulusan` untuk memisahkan tanggung jawab (SRP). |
| **Introduce Constant** | Kelas `KriteriaKelulusan` digunakan untuk mendefinisikan konstanta kriteria, membuatnya mudah diubah dan meningkatkan keterbacaan. |
| **Extract Method** | Memecah logika kompleks menjadi metode yang lebih kecil dan fokus (`cekStatus`, `tampilkanLaporan`). |
| **Rename Method** | Mengganti nama metode agar lebih deskriptif (`getHasilProses`). |
| **Simplify Conditional Logic** | Menggunakan struktur `if-else if-else` yang bersih dan eksplisit dalam `cekStatus`. |

## ⚙️ Persyaratan

* **Java Development Kit (JDK):** Versi 8 atau lebih tinggi.

## 🚀 Cara Menjalankan Program

1.  **Kompilasi:** Buka terminal dan navigasikan ke direktori tempat file `ProgramModular.java` berada.
    ```bash
    javac ProgramModular.java
    ```
2.  **Jalankan:**
    ```bash
    java ProgramModular
    ```

## 📜 Output Contoh

Program akan menghasilkan output laporan kelulusan seperti berikut:

```
--- LAPORAN KELULUSAN SISWA ---
Nama: Ani | Status: LULUS | Catatan: Memenuhi semua kriteria.
Nama: Budi | Status: TIDAK LULUS | Catatan: Nilai kurang dari 75.
Nama: Citra | Status: TIDAK LULUS | Catatan: Kehadiran kurang dari 80.
---------------------------------
```

## 🔑 Kriteria Kelulusan Saat Ini

Kriteria kelulusan yang diatur dalam kelas `KriteriaKelulusan` adalah:

* **Nilai Minimum:** 75
* **Kehadiran Minimum:** 80

Untuk mengubah kriteria ini, cukup modifikasi konstanta `MIN_NILAI` dan `MIN_KEHADIRAN` di kelas `KriteriaKelulusan`.

-----

