Task :
1. Penjelasan text manipulation beserta step by step
2. Penjelasan tool htop atau nmon



[1] text manipulation adalah proses memodifikasi atau mengubah isi dari sebuah file menggunakan command tertentu dalam hal ini mengunakan command gitbash untuk proses menanipulasi text
cat // Perintah cat digunakan untuk menampilkan isi file atau output teks ke konsol.
pada perinta cat juga dapat memasukkan file kedalam text lain contoh //cat ManipulationCommand ManipulationCommand01 > ManipulationCommand02 maka text pada file ManipulationCommand dan ManipulationCommand01 akan dimasukkan kedalam ManipulationCommand02.
![perintah cat](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/b73206e9-e7c4-459e-8f45-d6bf90c3f311)

sed // digunakan untuk melakukan operasi penggantian, penghapusan, atau manipulasi teks lainnya dalam file atau output teks.
sed -i 's/Hello/sudahbelajar/g' ManipulationCommand02 // perintah ini akan mengubah text "belajar" menjadi sudahbelajar
grep // perintah untuk melakukan pencarian sebuah text dalam sebuah file yang telah dibuat. caontoh grep sudahbelajar ManipulationCommand02
akan mencari text pada file ManipulationCommand02 "sudahbelajar"
![set, grep dan sort ](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/eafaec51-445c-42e9-842b-a4e5b0c368d8)

sort // perintah ini akan mengurutkan data
![perintah sort](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/1447126f-1a35-4370-b1f1-7b8dc22393c6)


echo// command echo disini tidak hanya mempu menampilkan text tetapi juga dapat replace semua data di file

![perinta echo](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/b41bbd7c-660b-4695-89af-22a694a7c353)

[2] dalam memonitoring  aktivitas untuk melihat kinerja sistem secara realtime dibutuhkan beberapa perintah salah satunya adalah htop dan nmon  digunakan untuk memonitoring sebuah server

htop seperti yang telah dijelaskan diatas htop digunakan untuk memonitoring  penggunaan memory, cpu, swap. gunakan perintah //htop pada ubuntu server


nmon sama halnya seperti htop, Berikut adalah tampilan dari nmon untuk menampilkan cpu, memory, disk, dan network


c adalah CPU
m adalah Memory
d adalah Disk
n adalah network



