### PRAKTIKUM 7
### USWATUN HASANAH
### 312210343
### TI.22.A3

###  MEMBUAT fungsi menggunakan lamda

```
import math
def a(x):
  return x**2
a = lambda x : x**2
print(a(2))
def b(x, y):
  return math.sqrt(x*2 + y*2)
b = lambda x, y : x * 2 + y * 2
print(b(2, 2))
def c(*args):
  return sum(args)/len(args)
c = lambda *args : sum(args)/len(args)
print(c(1,2,3,4,5))
def d(s):
  return "".join(set(s))
d = lambda s: "".join(set(s))
print(d("buku"))
```


### HASIL OUTPUTNYA

![latihan](https://user-images.githubusercontent.com/115516474/205488883-457935cd-50bc-4d80-bbed-d709b0860e6f.png)


### PRAKTIKUM DICTIONARY

### PENJELASAN TUGAS
1. MENAMBAHKAN DICTIONARY LALU INPUT DENGAN DATA `data={}`
2. MEMBUAT PELUANG FUNGSI DENGAN `DEF` UNTUK MENAMPILKAN  FUNGSI
3. LALU MENAMBAHKAN DATA NIM, NAMA, NILAI TUGAS UTS, DAN UAS. Data yang diimput akan masuk ke dictionary, data dengan Nama sebagai keys. 
   Sedangkan nim, tugas, san uts, uas akan menjadi data valiu.

```
x = mahasiswa = {}

def tambah():
    print("Tambah Data")
    nama = input("Masukkan Nama Mahasiswa   : ")
    nim = input("Masukkan NIM              : ")
    tugas = int(input("Masukkan Nilai Tugas      : "))
    uts = int(input("Masukkan Nilai UTS        : "))
    uas = int(input("Masukkan Nilai UAS        : "))
    akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
    mahasiswa[nama] = nim , tugas, uts , uas , akhir
 ```
 
 ![T](https://user-images.githubusercontent.com/115516474/205491861-a5e131fb-17d9-4e0d-9c74-f1d0a6f21a5b.png)

    
4. Menambahkan atau melihat data. sebelum melihat data kita harus mengimpu data terlebih dahulu agar data yang udah di imput bisa ditampilkan, 
jika belum mengimput data otomatis data yang ditampilkan akan bertuliskan tidak ada.

```
def tampilkan():
    if mahasiswa.items():
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        i = 0
        for b in mahasiswa.items():
             i += 1
             print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} | {5:7f}   |"
                . format ( b [ 0 ][: 14 ], b [ 1 ][ 0 ], b [ 1 ][ 1 ], b [ 1 ][ 2 ], b [ 1 ][ 3 ], b [ 1 ][ 4 ] , no = i ))
        print("---------------------------------------------------------------------------------")
    else :
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        print("|                                TIDAK ADA DATA                                 |")
        print("---------------------------------------------------------------------------------")
 ```
 
 ![L](https://user-images.githubusercontent.com/115516474/205491934-5298444a-d498-498b-b09b-e5d60a3c3323.png)

 
 5. Apabila ingin menghapus data maka kita akan diminta untuk mengimput nama terlebihdahulu, lalu data yang telah diimput akan dihapus 
 bersama nim, nilai tugas, nilai uts, nilai uas.
 
 
 ```
 def hapus():
    print ( "Hapus Data" )
    nama = input("Masukkan Nama Mahasiswa   : ")
    if  nama in  mahasiswa . keys ():
        del  mahasiswa [ nama ]
    else :
        print ( "Nama {0} Tidak Ditemukan" . format ( nama ))

```
 
 
 ![H](https://user-images.githubusercontent.com/115516474/205492015-e3ae1c25-c808-49b9-a65f-ce68daa7763b.png)
 

 6. Apabila ingin mengubah data, kita diminta untuk mengimput nama terlebihdahulu, barulah data bisa diubah.
 
 ```
 def ubah():
    print ( "Ubah Data" )
    nama = input("Masukkan Nama Mahasiswa   : ")
    if nama in  mahasiswa . keys ():
        nim = input("Masukkan NIM              : ")
        tugas = int(input("Masukkan Nilai Tugas      : "))
        uts = int(input("Masukkan Nilai UTS        : "))
        uas = int(input("Masukkan Nilai UAS        : "))
        akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
        mahasiswa[nama] = nim , tugas, uts , uas , akhir
    else :
        print ( "Nama{0} Tidak Ditemukan" . format(nama ))

 ```
 
 ![U](https://user-images.githubusercontent.com/115516474/205492038-09e9db1f-ae1d-4873-9b1d-86b4ed02574d.png)

   
7. Setelah selesai membuat program data di atas maka kita perlu mengulang statement menggunakan `while` yang terdapat pilihan menu untuk menjalankan program. 
    

```
while True:
    print("")
    print("===========================")
    print("|   Program Input Nilai   |")
    print("===========================")
    c = input("L)ihat, T)ambah, U)bah, H)apus, K)eluar: ")
    if c.lower() == "l":
        tampilkan()
    elif c.lower() == "t":
        tambah()
    elif c.lower() == "u":
        ubah()
    elif c.lower() == "h":
        hapus()
    elif c.lower() == "k":
        print()
        print("---------------------------------------------------------------------------------")
        print("                                 PROGRAM TELAH SELESAI                    ")
        print("---------------------------------------------------------------------------------")
        print(35*'=')
        print("Nama\t: USWATUN HASANAH\nKelas\t: TI.22.A3\nNIM\t\t: 312210343")
        print(35*'=')
        break

    else:
        print()
        print("Kode yang anda masukkan salah!")
```

![K](https://user-images.githubusercontent.com/115516474/205492185-c4f01fe7-7f45-4c24-802e-d56b611708b0.png)


### FLAWCHART

![Screenshot (164)](https://user-images.githubusercontent.com/115516474/205494798-03fa46c8-790a-4666-b50b-7390132e10c8.png)


