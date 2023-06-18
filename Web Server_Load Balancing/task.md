
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

![Screenshot 2023-06-18 211918](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/8a0a96c9-2293-44de-9f8b-8b1ab82ee4b3)


    - jalankan perintah sudo systemctl start nginx untuk menajalan nginx dan  sudo systemctl stop nginx untuk mematikan nginx
    - kita juga dapat melakukan perintan enable dan disable // sudo systemctl enable nginx // sudo systemctl disable nginx untuk menghidupkan dan mematikan sistem        nginx
![Screenshot 2023-06-18 211934](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/78c64f76-a3a8-4968-826e-56a9a224ec62)

    - untuk me-reload sistem dari Nginx gunakan perinta sudo systemctl restart nginx

[2] aplikasi dumbflix menggunakan PM2
    buat sebuah directory baru
    gunakan perinta git clone https://github.com/dumbwaysdev/dumbflix-frontend pada direcroty  yang baru saja dibuat
    install library PM2 pada ubuntu server dengan menjalankan perintah npm install pm2 -g
    masuk ke directory dumbflix-frontend masukakn perintah pm2 list untuk melihat semua app yang berjalan
    untuk menjalankan aplikasi gunakan perinta pm2 start app.js
