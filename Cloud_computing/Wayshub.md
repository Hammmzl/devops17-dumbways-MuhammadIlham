
Buat 2 VM di IDCloudHost dengan spesifikasi sebagai berikut :
   - Appserver : 2 CPU, 2 GB RAM
   - Gateway : 2 CPU, 1 GB RAM
   - Storage : 20 GB

Repository :
[Wayshub Frontend](https://github.com/dumbwaysdev/wayshub-frontend)
[Wayshub Backend](https://github.com/dumbwaysdev/wayshub-backend)


Tasks :
[ Appserver ]

    - Gunakan nodejs versi 14.x
    - Clone repository Wayshub frontend & backend lalu deploy aplikasinya menggunakan PM2
    - Install dan konfigurasi database MySQL (mysql_secure_installation)
    - Di wayshub-frontend, rubah isi BaseURL file src/config/api.js menggunakan domain yang sudah disediakan (api.<nama>.studentdumbways.my.id)
    - Di wayshub-backend, rubah isi konfigurasi database MySQL di config/config.json sesuai dengan user pass kalian, dengan nama database "db-wayshub"



[IDCH APP SERVER]
- Buat dua VM Pada IDCH, VM Pertama untuk app server dan VM kedua untuk gateway dengan spesifikasi diatas
- VM APPSERVER

![Screenshot 2023-07-08 223227](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/173d7d9d-8d75-4e04-bd19-4d8ccbe38e69)

         - VM GATEWAY
![Screenshot 2023-07-08 223240](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/832d368c-2a31-4caf-9bce-919c645b6348)

    - kemudian masuk ke terminal windows dan ssh dengan username dan ip yang telaha didibuat pada idch
 ![Screenshot 2023-07-08 223248](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/8dbf0090-efb7-475a-93b8-7d9ae17a5603)

      - setelah berhasil masuk, install curl pada vm (sudo apt install curl) command tersebut digunakan untuk mengecek konektivitas ke URL dan juga sebagai tool transfer data.
      - setelaha selesai jalan perintah curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash  untuk menginstall NVM pada VM.

   ![Screenshot 2023-07-08 223248](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/168f713c-6734-4c92-b1b5-ec147d30d325)

    - setelah berhasil diintall, selanjutnya install nvm versi 14 dengan perintah (nvm install 14) jika tidak berhasil jalankan perintah exec bash terlebihdahulu
   ![Screenshot 2023-07-08 223300](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/38d063b0-e4e1-4cdf-aa9d-2bfbc3be7417)


    - selanjutnya clone repository github yang telah disediakan diatas untuk frondend dan backendnya.
   ![Screenshot 2023-07-08 223306](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/bb93496f-d4ef-4eed-a392-a22fc7f0d752)

      - setalah clone repo berhasil, jelankan perintah (npm install -g pm2) untuk mengintall pm2 secara global pada vm
   ![Screenshot 2023-07-08 223314](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/f3e165d1-38a1-4153-a258-84feff1b9896)

      - masuk ke folder wayshub-frontend jalankan perintan (npm install), kemudian jalankan perintan (pm2 ecosystem init) untuk konfigurasi ecosystem pm2 dan generated file ecosystem.config.js
   ![Screenshot 2023-07-08 223424](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/87946dbe-fdd9-4fd1-91b8-8deb89ca1c8a)

      - ubah file ecosystem.config.js dengan perintah (nano ecosystem.config.js) pada bagian script ganti index.js ke npm run start
   ![Screenshot 2023-07-08 223329](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/1f9edbe8-0035-452c-b872-aaf07d982614)

      - kemudian jalankan pm2 start, kita dapat melihat pm2 yang berjalan dengan perintah (pm2 list)

   ![Screenshot 2023-07-08 223424](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/37aa29cb-69a7-4f4c-ad13-2208c63dbd9f)

    

      

