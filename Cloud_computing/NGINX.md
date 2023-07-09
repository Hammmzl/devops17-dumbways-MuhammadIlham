Buat 2 VM di IDCloudHost dengan spesifikasi sebagai berikut :
   - Appserver : 2 CPU, 2 GB RAM
   - Gateway : 2 CPU, 1 GB RAM
   - Storage : 20 GB

Tasks :
[ Gateway ]

    - Installasi nginx di server gateway
    - Buat konfigurasi reverse proxy di dalam directory : /etc/nginx/dumbways
    - Gunakan domain :
       - <nama>.studentdumbways.my.id (front-end)
       - api.<nama>.studentdumbways.my.id (back-end)
        note : <nama> diganti sesuai dengan nama kalian.



[Proses Instalasi NGINX di server gateway]


         - masuk ke vm gateway yang telah dibuat di idch pada terminal dengan ssh username@190.xxx.xx.xx
   ![Screenshot 2023-07-09 000258](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/8ed073ab-58d0-4ff9-b779-edc7c396fb89)

         - sudo apt update pada terminal gateway, selanjutnya jalankan perintah sudo apt install nginx tunggu hingga proses instalasi selesai
   ![Screenshot 2023-07-09 000308](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/37ce3a3d-1fa5-46af-afd8-a66701f0aeac)

         - jalankan perintah sudo systemctl status nginx untuk melihat status nginx  yang berjalan, kemudian masuk ke /etc/nginx dan buat file dengan nama ilham.cof (sebagai contoh) 
 ![Screenshot 2023-07-09 000322](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/a43c8693-c0e6-4180-9fad-bccc7f0b6434)

    
    lalu masukan query seperti pada gambar dibawah, ubah server name dan proxy pass sesuai dengan domain dan ip yang telah dibuat di cloudflare
   ![Screenshot 2023-07-09 000314](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/be63f2ae-444c-42e7-b456-6da21d680b95)

       - gunakan perintah sudo nginx -t untuk memeriksa konfigurasi nginx tanpa melalui server secara aktif kemudian jalan kan perinta reload nginx sudo systemctl reload nginx

   ![Screenshot 2023-07-09 000330](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/606c2e24-926c-42f2-8df1-0f34778f913a)

      - terakhir cek web yang telah di deploy dengan akses ke domain ilham.studentdumways.my.id dan cek api backand api.ilhamstudentdumways.my.id 
       
