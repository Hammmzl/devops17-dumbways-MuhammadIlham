
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

 
