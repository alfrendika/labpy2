# labpy2
Perulangan FOR
Digunakan ketika jumlah pengulangan sudah diketahui. Biasanya digunakan untuk mengulang item dalam urutan seperti list, string, atau range angka.
Contoh:

for i in range(5):
    print("Hello World!")


Perulangan WHILE
Digunakan ketika jumlah pengulangan belum diketahui, tetapi tergantung pada kondisi tertentu.
Contoh:

x = 0
while x < 5:
    print("Perulangan ke-", x + 1)
    x += 1


Perulangan Bersarang (Nested Loop)
Adalah perulangan di dalam perulangan lain. Biasanya digunakan untuk mengolah data dalam bentuk tabel, matriks, atau pola tertentu.
Contoh:

for i in range(3):
    for j in range(3):
        print(f"({i}, {j})")


Perulangan dengan Kondisi (Loop + If)
Menggabungkan logika if-else di dalam loop untuk menghasilkan keputusan setiap kali iterasi berlangsung.
Contoh:

for i in range(1, 6):
    if i % 2 == 0:
        print(f"{i} adalah bilangan genap")
    else:
        print(f"{i} adalah bilangan ganjil")
