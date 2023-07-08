
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
