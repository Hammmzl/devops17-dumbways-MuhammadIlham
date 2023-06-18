
Task :
1. Instalasi nginx melalui apt
2. menjalankan aplikasi dumbflix menggunakan PM2
3. buatlah konfigurasi reverse proxy!
(Gunakan 2 server untuk memenuhi challenge, tidak wajib)

Referensi :
- Nama Domain - dumbflix-<nama panggilan>.xyz
- Dumbflix-FE - ```https://github.com/dumbwaysdev/dumbflix-frontend```


[1] Proses instalasi nginx apt install nginx pada server  ubuntu
    - buka virtual machine ubuntu server jalankan perintah //sudo apt install nginx

    - setelah instalasi selesai jalankan perinta sudo //systemctl status nginx untuk melihat status nginx

    - jalankan perintah sudo systemctl start nginx untuk menajalan nginx dan  sudo systemctl stop nginx untuk mematikan nginx

    

    - kita juga dapat melakukan perintan enable dan disable // sudo systemctl enable nginx // sudo systemctl disable nginx untuk menghidupkan dan mematikan sistem        nginx

    - untuk me-reload sistem dari Nginx gunakan perinta sudo systemctl restart nginx

[2] plikasi dumbflix menggunakan PM2
  install PM2 pada 
