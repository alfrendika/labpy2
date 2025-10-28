# labpy2
Laporan Praktikum 2
Struktur Kondisi - Python
Nama: [Rahsya Alfrendika]
NIM: [312510339]
Kelas: [TI. 25.C.5]

Daftar Isi

Kasus 1: Program Pemesanan Tiket Bioskop
Kasus 2: Program Kalkulator Sederhana


Kasus 1: Program Pemesanan Tiket Bioskop
Deskripsi
Program ini menghitung harga tiket bioskop dengan ketentuan:

Tiket Reguler: Rp 50.000
Tiket VIP: Rp 100.000
Diskon 20% untuk member

Algoritma

START
Input tipe tiket (reguler/vip) dari user
Input status member (y/t) dari user
Tentukan harga tiket:

JIKA tipe_tiket = "reguler" MAKA harga = 50000
JIKA tipe_tiket = "vip" MAKA harga = 100000
JIKA TIDAK, harga = 0 (invalid)


Hitung diskon:

JIKA status_member = "y" MAKA diskon = 20%
JIKA TIDAK, diskon = 0%


Hitung total: total = harga - (harga × diskon)
Tampilkan detail pemesanan dan total harga
END

Flowchart
        ┌─────────┐
        │  START  │
        └────┬────┘
             │
        ┌────▼────────────────────┐
        │ Input tipe_tiket        │
        │ Input status_member     │
        └────┬────────────────────┘
             │
        ┌────▼─────────────────┐
        │ tipe_tiket ==        │
        │ "reguler"?           │
        └─┬────────────────┬───┘
      Ya  │                │ Tidak
          │                │
    ┌─────▼─────┐    ┌─────▼─────┐
    │ harga =   │    │ tipe ==   │
    │ 50000     │    │ "vip"?    │
    └─────┬─────┘    └─┬───────┬─┘
          │         Ya │       │ Tidak
          │       ┌────▼────┐  │
          │       │ harga = │  │
          │       │ 100000  │  │
          │       └────┬────┘  │
          │            │    ┌──▼──────┐
          │            │    │ harga = │
          │            │    │ 0       │
          │            │    └──┬──────┘
          └────────┬───┴───────┘
                   │
            ┌──────▼──────────┐
            │ status_member   │
            │ == "y"?         │
            └──┬──────────┬───┘
           Ya  │          │ Tidak
         ┌─────▼────┐  ┌──▼──────┐
         │ diskon = │  │ diskon =│
         │ 0.2      │  │ 0       │
         └─────┬────┘  └──┬──────┘
               └──────┬───┘
                      │
            ┌─────────▼─────────┐
            │ total = harga -   │
            │ (harga × diskon)  │
            └─────────┬─────────┘
                      │
            ┌─────────▼─────────┐
            │ Tampilkan detail  │
            │ dan total harga   │
            └─────────┬─────────┘
                      │
                 ┌────▼────┐
                 │   END   │
                 └─────────┘

Input Data:

Menggunakan .lower() untuk mengkonversi input ke huruf kecil agar tidak case-sensitive


Struktur Kondisi if-elif-else:

Memeriksa tipe tiket yang dipilih
Menentukan harga berdasarkan tipe


Operator Ternary:

diskon = 0.2 if status_member == "y" else 0
Sintaks singkat untuk memberikan nilai diskon


Perhitungan:

Total = harga - (harga × diskon)


Format Output:

Menggunakan f-string untuk format yang rapi
:, untuk menambahkan separator ribuan




Kasus 2: Program Kalkulator Sederhana
Deskripsi
Program kalkulator yang dapat melakukan operasi aritmatika dasar:

Penjumlahan (+)
Pengurangan (-)
Perkalian (*)
Pembagian (/)

Algoritma

START
Input angka pertama dari user
Input angka kedua dari user
Input operator (+, -, *, /) dari user
Proses perhitungan:

JIKA operator = "+" MAKA hasil = angka1 + angka2
JIKA operator = "-" MAKA hasil = angka1 - angka2
JIKA operator = "*" MAKA hasil = angka1 × angka2
JIKA operator = "/" MAKA

JIKA angka2 ≠ 0 MAKA hasil = angka1 ÷ angka2
JIKA TIDAK, tampilkan error


JIKA TIDAK, operator tidak valid


Tampilkan hasil perhitungan
END

Flowchart
        ┌─────────┐
        │  START  │
        └────┬────┘
             │
        ┌────▼─────────────┐
        │ Input angka1     │
        │ Input angka2     │
        │ Input operator   │
        └────┬─────────────┘
             │
        ┌────▼────────┐
        │ operator == │
        │ "+"?        │
        └─┬────────┬──┘
      Ya  │        │ Tidak
    ┌─────▼────┐  │
    │ hasil =  │  │
    │ a1 + a2  │  │
    └─────┬────┘  │
          │    ┌──▼───────┐
          │    │ operator │
          │    │ == "-"?  │
          │    └─┬──────┬─┘
          │   Ya │      │ Tidak
          │ ┌────▼───┐  │
          │ │ hasil= │  │
          │ │ a1-a2  │  │
          │ └────┬───┘  │
          │      │   ┌──▼───────┐
          │      │   │ operator │
          │      │   │ == "*"?  │
          │      │   └─┬──────┬─┘
          │      │  Ya │      │ Tidak
          │      │ ┌───▼───┐  │
          │      │ │ hasil=│  │
          │      │ │ a1*a2 │  │
          │      │ └───┬───┘  │
          │      │     │   ┌──▼───────┐
          │      │     │   │ operator │
          │      │     │   │ == "/"?  │
          │      │     │   └─┬──────┬─┘
          │      │     │  Ya │      │ Tidak
          │      │     │ ┌───▼────┐ │
          │      │     │ │ angka2 │ │
          │      │     │ │ != 0?  │ │
          │      │     │ └─┬────┬─┘ │
          │      │     │Ya │    │No │
          │      │  ┌────▼─┐ ┌─▼───┐│
          │      │  │hasil=│ │Error││
          │      │  │a1/a2 │ └─┬───┘│
          │      │  └────┬─┘   │    │
          │      │       │  ┌──▼────▼──┐
          │      │       │  │ Operator │
          │      │       │  │ Invalid  │
          │      │       │  └──┬───────┘
          └──────┴───────┴─────┘
                 │
          ┌──────▼────────┐
          │ Tampilkan     │
          │ hasil         │
          └──────┬────────┘
                 │
            ┌────▼────┐
            │   END   │
            └─────────┘

Input Data:

Menggunakan float() untuk menerima bilangan desimal
Input operator sebagai string


Struktur Kondisi if-elif-else:

Memeriksa operator yang dipilih secara berurutan
Setiap kondisi melakukan operasi aritmatika yang sesuai


Validasi Pembagian:

Nested if untuk memeriksa pembagian dengan nol
Mencegah error division by zero


Error Handling:

Menggunakan hasil = None untuk menandai operasi invalid
Menampilkan pesan error yang jelas


Output:

Menampilkan nama operasi, kedua angka, dan hasil
Menggunakan conditional untuk menampilkan hasil hanya jika valid


    ├── tiket_reguler.png
    ├── tiket_vip.png
    ├── kalkulator_tambah.png
    ├── kalkulator_bagi.png
    └── kalkulator_error.png
