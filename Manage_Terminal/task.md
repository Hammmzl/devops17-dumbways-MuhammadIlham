Task :
1. Penjelasan text manipulation beserta step by step
2. Penjelasan tool htop atau nmon



[1] text manipulation adalah proses memodifikasi atau mengubah isi dari sebuah file menggunakan command tertentu dalam hal ini mengunakan command gitbash untuk proses menanipulasi text
cat // Perintah cat digunakan untuk menampilkan isi file atau output teks ke konsol.
pada perinta cat juga dapat memasukkan file kedalam text lain contoh //cat ManipulationCommand ManipulationCommand01 > ManipulationCommand02 maka text pada file ManipulationCommand dan ManipulationCommand01 akan dimasukkan kedalam ManipulationCommand02.

set // digunakan untuk melakukan operasi penggantian, penghapusan, atau manipulasi teks lainnya dalam file atau output teks.
sed -i 's/Hello/sudahbelajar/g' ManipulationCommand02 // perintah ini akan mengubah text "belajar" menjadi sudahbelajar
grep // perintah untuk melakukan pencarian sebuah text dalam sebuah file yang telah dibuat. caontoh grep sudahbelajar ManipulationCommand02
akan mencari text pada file ManipulationCommand02 "sudahbelajar"

sort // perintah ini akan menngurutkan data


echo// command echo disini tidak hanya mempu menampilkan text tetapi juga dapat replace semua data di file


