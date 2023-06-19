
Task :
1. Perbandingan antara Monolith & Microservices
2. Deploy Aplikasi wayshub-frontend (NodeJS)
3. Deploy Golang & Python dengan menampilkan nama masing-masing

Repository
```https://github.com/dumbwaysdev/wayshub-frontend```


[1] Monolith, Perubahan pada salah satu bagian aplikasi dapat mempengaruhi seluruh sistem, sehingga pengembangan dan pengujian dapat menjadi lebih rumit. Microservice,  Setiap layanan mikro dapat dikembangkan, diperbarui, dan dideploy secara independen, yang memungkinkan tim pengembang untuk fokus pada layanan tertentu tanpa mengganggu layanan lain.

[2] Deploy Aplikasi wayshub-frontend (NodeJS)

  - clone repo dari https://github.com/dumbwaysdev/wayshub-frontend

  - ![Screenshot 2023-06-18 201637](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/ea0dcae4-eaf9-4152-9419-35ae0b1b388f)


  - install npm versi 16 untuk menjalankan wayshub-frontend //npm install 16 // jika terdapat lebih dari satu versi npm gunakan perintan // npm use 16
  - gunakan perintah npm i untuk menginisialisasi project wayshub-frontend (NodeJS)
  - ![Screenshot 2023-06-18 201643](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0879bc75-5f42-4f17-8389-ded10cf41b66)





   - untuk menjalankannya di web server gunakan perintah // npm run start
     ![Screenshot 2023-06-18 201617](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/ed77aa1b-8ab2-4ee2-9cb1-3693f0ae972d)



  - untuk melihat  aplikasi yang berjalan buka web browser dan masukan ip add server serta port yang berjalan // 172.20.10.8:3000
   
  - ![Screenshot 2023-06-18 201631](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/9a8bbfea-9ac8-40c8-b0a9-5e9d2c1d0762)








[3] Deploy Golang

// download engine-nya terlebih dahulu wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit
![go2](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/b69e2c5e-e978-4829-92ef-36c2532f318c)

masukkan path go pada .bashrc // sudo nano .bashrc
export PATH=$PATH:/usr/local/go/bin 
![go1](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/4defa43d-12a4-4c6d-b025-8448cbfadc52)


Verifikasi go dengan cara berikut: 
-go version untuk membuat aplikasi sederhana dengan go, Buat sebuah file dengan nama index.go. // nano index.go
-Setelah itu masukkan script dibawah ini.
 index.go
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
![go3](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/091452fd-672b-4c66-a499-d7a78b04f8f9)


- selanjutnya jalankan aplikasi go dengan perintah // go  run index.go
- jika aplikasi ingin di build jalankan perintah // go build index.go
- jika sudah berjalan gunakan perintah ./index

![go4](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0ad9d036-e864-4d85-bdc7-43ab5609e10f)


 // Deploy python //
 - install python3 //sudo apt update; sudo apt upgrade
 - python3 secara default telah terintal pada ubuntu server, cek python3 // python3 -v
 - install package manager dari python3 //sudo apt install python3-pip
    ![py01](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0ad2000b-bb0d-4723-b591-0a7683ec72fd)

   
 - kemudian install flask //pip install flask.
   ![py02](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/c9b03adc-468d-4948-9c72-932bd11a032d)

 - Untuk mencetak text sederhana menggunakan Python3.
 - buat terlebih dahulu file dengan nama index.py masukan script
    from flask import Flask
    app = Flask(__name__)
    @app.route("/")
    def helloworld():
        return "Hello World"
    if __name__ == "__main__":
    app.run()

   perlu di ingat sesuaikan pada app.run gunakan host sesuai dengan ip dan dan juga tidak bisa berjalan gunakan perintah //sudo ufw allow 5000 untuk mengizinkan run di port 5000
![py03](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/254e2190-3c88-4e9f-8e75-94ee90108923)

   
 - untuk menjalankan aplikasi //python3 index.py
 - gunakan web browser akses dengan localhost:5000
![py04](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/6c410ebe-7f14-4b67-bde3-c4ff0c8a7873)
