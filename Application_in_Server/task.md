
Task :
1. Perbandingan antara Monolith & Microservices
2. Deploy Aplikasi wayshub-frontend (NodeJS)
3. Deploy Golang & Python dengan menampilkan nama masing-masing

Repository
```https://github.com/dumbwaysdev/wayshub-frontend```


[1] Monolith, Perubahan pada salah satu bagian aplikasi dapat mempengaruhi seluruh sistem, sehingga pengembangan dan pengujian dapat menjadi lebih rumit. Microservice,  Setiap layanan mikro dapat dikembangkan, diperbarui, dan dideploy secara independen, yang memungkinkan tim pengembang untuk fokus pada layanan tertentu tanpa mengganggu layanan lain.

[2]




[3] Deploy Golang // download engine-nya terlebih dahulu wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit
masukkan path go pada .bashrc // sudo nano .bashrc
export PATH=$PATH:/usr/local/go/bin 

Verifikasi go dengan cara berikut: 
-go version untuk membuat aplikasi sederhana dengan go, Buat sebuah file dengan nama index.go. // nano index.go
-Setelah itu masukkan script dibawah ini.
 index.go
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}

- selanjutnya jalankan aplikasi go dengan perintah // go  run index.go
- jika aplikasi ingin di build jalankan perintah // go build index.go
- jika sudah berjalan gunakan perintah ./index

 // Deploy python //
 - install python3 //sudo apt update; sudo apt upgrade
 - python3 secara default telah terintal pada ubuntu server, cek python3 // python3 -v
 - install package manager dari python3 //sudo apt install python3-pip
 - kemudian install flask //pip install flask
 - Untuk membuat aplikasi sederhana menggunakan Python3.
 - buat terlebih dahulu file dengan nama index.py masukan script
    from flask import Flask
    app = Flask(__name__)
    @app.route("/")
    def helloworld():
        return "Hello World"
    if __name__ == "__main__":
    app.run()
 - untuk menjalankan aplikasi //python3 index.py
 - gunakan web browser akses dengan localhost:5000
