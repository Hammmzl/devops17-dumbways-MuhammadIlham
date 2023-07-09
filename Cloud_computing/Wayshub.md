
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
- VM APPSERVER masukan public key SSH id_rsa.pub

![Screenshot 2023-07-08 223227](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/173d7d9d-8d75-4e04-bd19-4d8ccbe38e69)

         - VM GATEWAY
![Screenshot 2023-07-08 223240](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/832d368c-2a31-4caf-9bce-919c645b6348)

    - kemudian masuk ke terminal windows jalankan perintah sudo apt update dan ssh dengan username dan ip yang telaha didibuat pada idch
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

[WAYSHUB - FRONTEND]

      - masuk ke folder wayshub-frontend jalankan perintan (npm install), kemudian jalankan perintan (pm2 ecosystem init) untuk konfigurasi ecosystem pm2 dan generated file ecosystem.config.js
   ![Screenshot 2023-07-08 223424](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/87946dbe-fdd9-4fd1-91b8-8deb89ca1c8a)

      - ubah file ecosystem.config.js dengan perintah (nano ecosystem.config.js) pada bagian script ganti index.js ke npm run start
   ![Screenshot 2023-07-08 223329](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/1f9edbe8-0035-452c-b872-aaf07d982614)

      - kemudian jalankan pm2 start, kita dapat melihat pm2 yang berjalan dengan perintah (pm2 list)

   ![Screenshot 2023-07-08 223424](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/37aa29cb-69a7-4f4c-ad13-2208c63dbd9f)

    - buka web browser untuk mengecek web frontend dengan ip public idch dan port 3000

   ![Screenshot 2023-07-08 223336](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/a09f2491-c554-4a79-a656-15f02715287b)

[WAYSHUB BACKEND]

    - sama halnya seperti pada frontend konfigurasi backend menggunakan npm install kemudian (pm2 ecosystem init) untuk generated file ecosystem.config.js
    ubah file cosystem.config.js pada bagian script ganti ke npm start bedakan dengan script ecosystem.config.js. jalankan perintah pm2 start dan pm2 list untuk melihat pm2 yang berjalan
   ![Screenshot 2023-07-08 231455](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/c2ead59b-b0ed-4480-9bb7-9cd0cf66b4c6)

   ![Screenshot 2023-07-08 231443](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/3c4a7914-ba02-4521-8ed8-fed38565fe27)

      - untuk mengecek backand pada web browser gunakan ip dan port 5000 untuk backand, jika muncul cannot get maka backand telah berhasil dijalankan

![Screenshot 2023-07-08 231510](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/68347f00-e908-48f4-8f1f-50e9776a126b)


[Install dan konfigurasi database MySQL (mysql_secure_installation)]
   - masuk ke terminal pastikan masuk ke appserver jalankan perintah (sudo apt install mysql-server) untuk konfigurasi, mengunduh paket MySQL Server dan dependensinya.
![Screenshot 2023-07-08 231533](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/be783e6a-c9eb-4132-9e0d-166cf52eaadb)

    - selanjutnya jalankan perintah (sudo systemctl start mysql.service) digunakan untuk memulai layanan MySQL pada sistem Linux.
![Screenshot 2023-07-08 231546](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/95970899-433f-4434-95b3-73d156953d1d)

    - gunakan perintah sudo mysql, setalah masuk ke mysql gunakan perintah ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'; untuk mengubah kata sandi pengguna root MySQL disini passwordnya adalah 'password' kemudian exit
![Screenshot 2023-07-08 231552](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/99f55487-b49a-4709-b7c6-02c9a6af2743)

    - masuk ke user root dengan perintah sudo mysql -u root -p dan masukkan password yang telah dibuat.
![Screenshot 2023-07-08 231607](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/f21a8b16-b1c9-402e-842d-9b6bee5824e9)
      
      - gunakan perintah CREATE USER 'ilham'@'%' IDENTIFIED BY '12345678' perintah tersebut membuat user baru dengan nama ilham dan localhost diganti ke '%'
      dan '12345678' adalah password yang telah dibuat.
      - selanjutnya jalanmkan perintah GRANT ALL PRIVILEGES ON database_name.* TO 'username'@'localhost' IDENTIFIED BY 'password'; digunakan untuk memberikan semua hak akses (privilege) kepada pengguna sebagai contoh disini ilham.
   ![Screenshot 2023-07-08 231613](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/115c8ad3-ffca-4bee-b1da-9507d751ef7f)

    -kemudian exit, jalankan perintah (sudo mysql -u ilham -p) untuk masuk ke user ilham yang telah dubuat.
   ![Screenshot 2023-07-08 234244](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/e234ada7-dcbe-4064-b194-317cb19e46c5)

      - ada beberapa perintah dalam mysql sepertin SHOW  DATABASES untuk melihat database dan CREATE DATABASE <database name> untuk membuat databases baru.
   ![Screenshot 2023-07-08 234253](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/834cec20-16cc-4463-87bc-8a6a0bd1b4a4)

    - setelah membuat database dan exit, masuk ke wayshub-frontend jalankan perintah nano src/config/api.js ubah base url ke (api.<nama>.studentdumbways.my.id) yang telah dibuat dicloudflare. 
   ![Screenshot 2023-07-08 234322](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/9aa08567-4a6f-483c-b46c-c604863d7a3d)

      - file src/config/api.js yang diubah
   ![Screenshot 2023-07-08 234305](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0f6b640c-4b33-4321-aaa0-23b50a81237a)

     -selnajutnya masuk kembali ke wayshub-backand ubah file config/config.json untuk mengkoneksikan database ke backand ubah username password dan name database yang talah dibuat.

   ![Screenshot 2023-07-08 234312](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/5dedda7a-fcdc-4322-a4c4-749cf685e600)

    - kemudian gunakan perintah  (npm i  -g sequelize-cli) perintah ini digunakan untuk menginstal paket Sequelize CLI secara global menggunakan npm (Node Package Manager) selanjutnya jalankan perintah (sequelize db:migrate) untuk  mencari dan menjalankan file migrasi yang ada dalam proyek. 
   ![Screenshot 2023-07-09 004725](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/c4621817-040f-47e5-847c-6eaadeaf8df8)

      
    selanjutnya kita sudah dapat mengunakan aplikasi web wayshub 
   ![Screenshot 2023-07-08 234334](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0f3d73f6-6161-423e-b2c2-4cf0cff94d90)

 



      

