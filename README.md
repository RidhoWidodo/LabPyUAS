# LabPyUAS

*Nama   :Muhammad Ridho Hafiedz*

*Nim    :31241095*

*Kelas  :24.A.2*

*Matkul :Bahasa Pemrograman*

**Project Python: Sistem Kasir Sederhan**

    #Program Kasir Sederhana
    def tampilkan_menu():
        print("=== Menu Kasir ===")
        print("1. Tambah Item")
        print("2. Tampilkan Struk")
        print("3. Keluar")
        
    def tambah_item(keranjang):
        nama_item = input("Masukkan nama item: ")
        harga_item = float(input("Masukkan harga item: "))
        jumlah_item = int(input("Masukkan jumlah item: "))
     #Menambahkan item ke dalam keranjang
     keranjang[nama_item] = {
           'harga': harga_item,
           'jumlah': jumlah_item
       }
      print(f"Item '{nama_item}' berhasil ditambahkan ke keranjang.")
      
     def tampilkan_struk(keranjang):
         print("\n=== Struk Pembayaran ===")
         total = 0
         for item, detail in keranjang.items():
              subtotal = detail['harga'] * detail['jumlah']
              total += subtotal
              print(f"{item} - Harga: {detail['harga']} x Jumlah: {detail['jumlah']} = Subtotal: {subtotal}")

               
         print(f"\nTotal Pembayaran: {total}")
         print("========================")

     def main():
        keranjang = {}
        while True:
           tampilkan_menu()
           pilihan = input("Pilih menu (1/2/3): ")

            if pilihan == '1':
               tambah_item(keranjang)
            elif pilihan == '2':
               tampilkan_struk(keranjang)
            elif pilihan == '3':
               print("Terima kasih! Sampai jumpa.")
               break
            else:
               print("Pilihan tidak valid! Silakan coba lagi.")

    if __name__ == "__main__":
      main()

**Berikut ini adalah Penjelasannya**

