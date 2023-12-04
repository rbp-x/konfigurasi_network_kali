# konfigurasi_network_kali
Cara Mengkonfigurasi Network Kali Linux di Virtual Box

Sebelumnya, jika mengalami kendala pada saat membuka Kali Linux pada virtual Box seperti dibawah ini, 

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/3cfb626c-8caa-44dc-8953-effc519111c4)

Solusinya adalah melakukan Disable dan Update pada Device Manager Network Adapter Virtual Box Only seperti pada gambar dibawah ini :

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/064a46b8-5fc4-491e-8981-04d3cb0ca27a)

Dengan actatan pada pengaturan jaringan / network pada Virtual Box seperti pada gambar dibawah ini :

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/538bcad4-317b-4cb9-8e8f-8518f500679e)

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/3f4d3e36-a5c7-402b-872f-a09448208c65)

# Pertama
Pastikan laptop/PC sudah mendapatkan IP Address, disini saya sudah mendapatkan IP 

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/ad8366a8-fe07-4e46-b1c9-fa5dec66d9a8)

# Kedua 
Setting jaringan di virtual box menjadi adaptor ter-brigde :

buka interfaces network menggunakan perintah pada CLI Kali :

  $ nano /etc/network/interfaces

## Tambahkan skrip pada file interfaces tersebut seperti dibawah ini :
  
  $ auto eth0 
  
  $ inet eth0 inet static
  
            address 192.-.-.-
  
            netmask 255.255.255.0
            
            network 192.-.-.-
            
            gateway 192.-.-.-
            
            dns-nameservers gugel

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/85719616-e318-477e-a3e7-d189fb363e80)


      ~ Keluar dan Simpan 

      Lakukan Restart dengan perintah :

      $ service networking restart 
      
![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/32394203-25ba-4ba3-a8e6-3c93c9cfd373)

      $ Test ping :

![image](https://github.com/rbp-x/konfigurasi_network_kali/assets/2045755/5394298d-f84f-42fe-9be8-bf1264910fa3)

# SUKSES !!




      
  


