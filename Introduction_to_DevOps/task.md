Task :
1. Definisi DevOps
2. sebutkan lifecycle DevOps (Continuous ...) dan Jelaskan definisi-definisinya!
3. Installasi Ubuntu Server menggunakan VMWare


(1) DevOps merupakan penyatuan atau penggabungan divisi, proses dan teknologi dalam fase pembuatan perangkat lunak antara development yang bertanggung jawab   
    mengurus (merancang dan modifikasi) sebuah aplikasi dengan operator yang memastikan aplikasi beroperasi secara optimal.
    
(2) - Continuous Integration (Integrasi Berkelanjutan): Prinsip ini mengacu pada praktik terus-menerus mengintegrasikan kode dari berbagai pengembang ke dalam 
      repositori 
      bersama secara sering dan otomatis.
    - Continuous Deployment (Penyediaan Berkelanjutan): Prinsip ini mendorong otomatisasi dalam penerbitan perangkat lunak ke lingkungan produksi secara terus-           menerus.
    - Continuous Testing (Pengujian Berkelanjutan): Prinsip ini melibatkan pelaksanaan tes secara terus-menerus selama siklus pengembangan perangkat lunak.
    - Continuous Monitoring (Pemantauan Berkelanjutan): Prinsip ini mendorong pemantauan terus-menerus terhadap sistem produksi, infrastruktur, dan kinerja               aplikasi.
    - Continuous Feedback (Umpan Balik Berkelanjutan): Prinsip ini menekankan pentingnya umpan balik yang terus-menerus antara tim pengembang dan tim operasi.
    - Continuous Development (Pengembangan Berkelanjutan) adalah pendekatan dalam praktik pengembangan perangkat lunak yang menekankan pada pengiriman perubahan          dan pembaruan perangkat lunak secara berkelanjutan.
    - Continuous Operations (Operasi Berkelanjutan) dalam konteks DevOps merujuk pada praktik-praktik dan pendekatan yang digunakan untuk menjaga operasional             sistem secara berkelanjutan setelah perangkat lunak diterapkan ke dalam lingkungan produksi.

(3) Installasi Ubuntu Server menggunakan VMWare

- Sebelum melakukan instalasi terlebih dahulu download  VMWare dan iso ubuntu servel di halaman resminya
   ![01](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/a634790a-8f0d-44e8-bbd1-a63978d07741)
   
    
- web resmi ubuntu untuk downlaod iso
    ![02](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/df47d724-2306-4ed1-b5a6-c9f802967251)

- buka VMWARE pada halama home dan create a new virtual machene
   ![03](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/3e68a48a-a326-413b-87d7-d9762eb03bac)
 
- muncul tampilan new virtual machine wizard, pada install form pilih disc image file iso yang telah didownload, seanjutnya klik next
  ![04](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/5491f85d-5b34-460c-af53-bdd7d0999053)
  
- kemudian isi form personal linux dengan nama, username dan password untuk login ke virtual machine
  ![05](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/d3a14880-e391-4ecb-ab47-60949aac1e71)


- pada virtual machine name isi sesuai dengan keinginan dan nantinya akan membuat file dengan nama tersebut
  ![06](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/e6ba85fd-14cb-43b9-b57f-756fbff5760d)

- selanjutnya atur maximum disk sesuai kebutuhan dan sesuaikan dengan spesifikasi laptop
    ![07](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/cad01091-81af-44d2-bde0-f076ac02adbe)

- kemudian akan muncul detail informasi tentang virtual machine yang telah dibuat, pilih costumize hardware
    ![08](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/4c53064f-ca1a-488e-9c50-f5401d210d68)

- akan muncul tampilan hardware sesuaikan antara memory dan processors, pada bagian  network adapter ganti nat ke bridged dan setting configure adapters yang sesuai
    ![09](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/5effa30a-39d8-4ae2-a618-14b2f13db1f0)

- tunggu hingga proses installasi selesai
    ![10](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/d36a5ccf-3fc3-43c0-89cc-d8d761f7f374)

- Pilih bahasa yang digunakan
    ![11](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/9fdabc76-ba59-41f7-a414-b952d20a55e5)

- pengaturan untuk keyboard layout pilih default english dan klik done
    ![12](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/9437f32e-f67a-43f2-9b00-268e40d6e0fb)

- Tampilan untuk mengatur network connection, pada bagian ini bisa memilih konfigurasi otomatis (DHCP AUTO) atau Setting manual IPv4
    ![13](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/ec706fb7-ec78-429e-a907-e70343e6a8e2)

- configure proxy bisa di kosongkan dan klik done
    ![14](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/955171b7-e1cc-4931-a516-b4074ee7d9df)

- pada configure  ubuntu archive mirror gunkan default address ubuntu
    ![15](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/f69f19de-db00-4bd4-a78c-b9b65b08877a)

- storage configuration klik use an entire disk
    ![16](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/8b26c0f3-1dae-42d7-a35c-4c5255214dc1)


- kemudian akan muncul storage configuration, kita juga dapat mengatur ulang dan membagi partisi dengan size yang di inginkan
    ![17](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/ae1109a8-4771-47ff-a347-50b3b287f21a)

- setup profile isi kembali nama pengguna, nama server, username dan password
    ![18](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0ed8a494-19c0-42dc-8c80-c0a269eb315d)

- pada settingan ssh setup klik install OpenSSH server, ssh server akan diinstall bersamaan dengan installasi ubuntunya
    ![19](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/cb67245f-27bc-4ded-a935-7aec8333f71a)

- tunggu hingga installasi sistem selesai
    ![20](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/295a05ad-2ac0-4628-843c-ba5d1738bc07)


- untuk cek koneksi ubuntu server anda dapat melakukan ping ke 8.8.8.8
    ![21](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/0538daff-efe3-451a-affe-2cf0c3f57744)
















  
   
