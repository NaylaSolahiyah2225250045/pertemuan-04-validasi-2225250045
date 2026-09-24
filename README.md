# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input

Nama: Nayla Solahiyah
NIM: 2225250045
Kelas: 3A

## Tujuan
Membangun program validasi dan klasifikasi nilai akhir dengan rantai if-elif-else.

## Cara Menjalankan
python3 praktik/validasi_klasifikasi_nilai.py

## Tabel Keputusan

| Kategori | Syarat | Contoh Masukan |
|---|---|---|
| Penolakan tipe | Ada data yang bukan angka | ujian=80, tugas=80, hadir=abc |
| Penolakan nilai ujian | Nilai ujian < 0 atau > 100 | ujian=105, tugas=80, hadir=90 |
| Penolakan nilai tugas | Nilai tugas < 0 atau > 100 | ujian=80, tugas=-5, hadir=90 |
| Penolakan kehadiran | Kehadiran < 0 atau > 100 | ujian=80, tugas=80, hadir=105 |
| Tidak memenuhi syarat kehadiran | Kehadiran < 80 | ujian=90, tugas=90, hadir=75 |
| Predikat A | Nilai akhir >= 85 dan kehadiran >= 80 | ujian=90, tugas=80, hadir=95 |
| Predikat B | Nilai akhir >= 70 dan < 85 serta kehadiran >= 80 | ujian=75, tugas=70, hadir=85 |
| Predikat C | Nilai akhir >= 60 dan < 70 serta kehadiran >= 80 | ujian=60, tugas=60, hadir=80 |
| Predikat D | Nilai akhir >= 50 dan < 60 serta kehadiran >= 80 | ujian=55, tugas=50, hadir=90 |
| Predikat E | Nilai akhir < 50 dan kehadiran >= 80 | ujian=40, tugas=30, hadir=100 |

## Hasil Pengujian

| No. | Masukan | Keluaran yang Diharapkan | Keluaran Aktual | Status |
|---|---|---|---|---|
| 1 | Ujian=90, Tugas=80, Kehadiran=95 | Nilai akhir 86.00, Predikat A, Lulus | Nilai akhir 86.00, Predikat A, Lulus | Lulus |
| 2 | Ujian=75, Tugas=70, Kehadiran=85 | Nilai akhir 73.00, Predikat B, Lulus | Nilai akhir 73.00, Predikat B, Lulus | Lulus |
| 3 | Ujian=60, Tugas=60, Kehadiran=80 | Nilai akhir 60.00, Predikat C, Lulus | Nilai akhir 60.00, Predikat C, Lulus | Lulus |
| 4 | Ujian=55, Tugas=50, Kehadiran=90 | Nilai akhir 53.00, Predikat D, Belum lulus | Nilai akhir 53.00, Predikat D, Belum lulus | Lulus |
| 5 | Ujian=40, Tugas=30, Kehadiran=100 | Nilai akhir 36.00, Predikat E, Belum lulus | Nilai akhir 36.00, Predikat E, Belum lulus | Lulus |
| 6 | Ujian=90, Tugas=90, Kehadiran=75 | Nilai akhir 90.00, Tidak memenuhi syarat kehadiran | Nilai akhir 90.00, Tidak memenuhi syarat kehadiran | Lulus |
| 7 | Ujian=105, Tugas=80, Kehadiran=90 | Penolakan rentang nilai ujian | Penolakan rentang nilai ujian | Lulus |
| 8 | Ujian=80, Tugas=-5, Kehadiran=90 | Penolakan rentang nilai tugas | Penolakan rentang nilai tugas | Lulus |
| 9 | Ujian=80, Tugas=80, Kehadiran=abc | Penolakan tipe | Penolakan tipe | Lulus |

## Refleksi
Masukan `abc` pada kehadiran bukan angka, sehingga tidak bisa diproses. Program menolaknya dengan `try-except` dan menampilkan pesan bahwa masukan harus berupa angka.

## Referensi
- RPS Algoritma dan Pemrograman OBE Untirta. Dokumen Program Studi, Tahun Ajaran 2026/2027 Ganjil.
- Downey, A. B. (2015). Think Python: How to Think Like a Computer Scientist (2nd ed.). Green Tea Press.
- Sweigart, A. (2019). Automate the Boring Stuff with Python (2nd ed.). No Starch Press.
- Python Software Foundation. Python Tutorial: More Control Flow Tools.
- Python Software Foundation. Python Tutorial: Errors and Exceptions.
- Visual Studio Code. Python Tutorial dan Python Debugging.