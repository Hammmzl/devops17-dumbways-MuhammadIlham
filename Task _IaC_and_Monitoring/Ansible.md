Sebelum mengerjakan tugas, mohon persiapkan :
- Akun Github dan buat repository dengan judul "devops17-dw-<nama kalian>"
- Gunakan file README.md untuk isi tugas kalian
- Buatlah langkah-langkah pengerjaan tugas beserta dokumentasinya

Buat 3 VM di IDCloudHost dengan **Terraform** spesifikasi sebagai berikut :
   - Appserver : 2 CPU, 1 GB RAM
   - Gateway : 2 CPU, 1 GB RAM
   - Monitoring : 2 CPU, 2 GB RAM
   - Storage : 20 GB

Tasks :

**[Local]**
buat konfigurasi Ansible & dan lakukan semua setup melalui local sebanyak mungkin.

**[appserver]**
gunakan ansible-playbook
- Membuat user baru, gunakan login ssh key
- Instalasi Docker & node-exporter
- Gunakan docker-compose untuk deploy aplikasi wayshub-frontend

**[gateway]**
gunakan ansible-playbook
- Membuat user baru, gunakan login ssh key
- Instalasi nginx
- Buat konfigurasi proxy lalu masukkan kedalam gateway

**[monitoring]**
buat konfigurasi prometheus
- monitor CPU & RAM untuk appserver
- monitor network untuk gateway
