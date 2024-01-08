# UAS-B.-PEMROGRAMAN

# daftar makanan dan minuman
makanan = {
    1: {"nama": "nasi goreng", "harga": 15000},
    2: {"nama": "mie ayam", "harga": 13000},
    3: {"nama": "ayam bakar", "harga": 15000},
    4: {"nama": "sate ayam", "harga": 18000},
    5: {"nama": "gado gado", "harga": 12000},

}

minuman = {
    1: {"nama": "es teh", "harga": 5000},
    2: {"nama": "es jeruk", "harga": 6000},
    3: {"nama": "kopi", "harga": 5000},
    4: {"nama": "air mineral", "harga": 3000},
    5: {"nama": "es cendol", "harga": 10000},

}

# fungsi untuk mencetak struk
def cetak_struk(nama, pesanan, total, uang):
    print("==============================")
    print("Nama pembeli:, {nama}")
    print("------------------------------")
    print("{:<20} {:<10} {:<5}".format('item', 'jumlah', 'harga'))
    print("------------------------------")
    for item, detail in pesanan.items():
        print("{:<20} {:<10} Rp {:<10}".format(item, detail['jumlah'], detail['harga']))
    print("------------------------------")
    print("{:<31} {:<20}".format('total', 'Rp '+str(total)))
    print("{:<31} {:<20}".format('uang', 'Rp '+str(uang)))
    print("{:<31} {:<20}".format('kembalian', 'Rp '+str(uang-total)))
    print("==============================")
    print("         TERIMA KASIH         ")

# fumgsi umtuk menampilkan menu dalam bentuk tabel
def tampilkan_menu(daftar):
    print("{:<5} {:<20} {:<10}".format('no', 'nama', 'harga'))
    print("------------------------------")
    for nomor, detail in daftar.items():
        print("{:<5} {:<20} Rp {:<10}".format(nomor, detail['nama'], detail['harga']))

# fungsi untuk program kasir
def kasir():
    while True:
        nama = input("\nMasukan nama pembeli: ")
        if nama.lower() == 'selesai':
            break
        pesanan ={}
        total  = 0
        while True:
            print("\nMenu makanan:")
            tampilkan_menu(makanan)
            print("6. selesai(ketik '0' untuk lanjut ke menu minuman)")
            pilihan = int(input("masukan pilihan anda: "))
            if pilihan == 0:
                break
            elif pilihan in makanan:
                jumlah = int(input("masukan jumlah: "))
                pesanan[makanan[pilihan]['nama']] = {'harga': makanan[pilihan]['harga']*jumlah, 'jumlah': jumlah}
                total += makanan[pilihan]['harga']*jumlah
            else:
                print("Maaf, pilihan tidak ada!")
        while True:
            print("\nMenu minuman:")
            tampilkan_menu(minuman)
            print("6. selesai(ketik '0' untuk mengakhiri pesanan)")
            pilihan = int(input("masukan pilihan anda: "))
            if pilihan == 0:
                break
            elif pilihan in minuman:
                jumlah = int(input("masukan jumlah: "))
                pesanan[makanan[pilihan]['nama']] = {'harga': minuman[pilihan]['harga']*jumlah, 'jumlah': jumlah}
                total += minuman[pilihan]['harga']*jumlah
            else:
                print("Maaf, pilihan tidak ada!")
        print("\nTotal harga : Rp ",total)
        uang = int(input("masukkan jumlah uang: "))
        cetak_struk(nama, pesanan, total, uang)

# jalankan program kasir
kasir()
![Screenshot (200)](https://github.com/Reardhyan/UAS-B.-PEMROGRAMAN/assets/148032571/d566daf6-db32-455b-a8d4-4a765c7c913f)
![Screenshot (201)](https://github.com/Reardhyan/UAS-B.-PEMROGRAMAN/assets/148032571/6005d1b1-403a-4452-9d4d-d22ee2d66acc)
![Screenshot (202)](https://github.com/Reardhyan/UAS-B.-PEMROGRAMAN/assets/148032571/fe16e79d-e936-4ce2-bf67-d5e31eaf185b)
![Screenshot (203)](https://github.com/Reardhyan/UAS-B.-PEMROGRAMAN/assets/148032571/b65bbf23-e988-4d4e-a7bb-141c69911553)

# link youtube
https://youtu.be/7EHyBLsyQuo?si=oRQtbPhuLLHbbK7i


