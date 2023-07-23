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
1. Install & jalankan Terraform di Local masing-masing
2. Buat terraform script untuk semua pembuatan server
3. Gunakan registry bapung/idcloudhost


INSTALASI TERRAFORM

Proses instalasi dan menjalankan terraform di local

- Pertama, instal dependensi yang diperlukan menggunakan perintah berikut:    
      
        apt-get install wget curl unzip software-properties-common gnupg2 -y

   ![1](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/cd0a6e52-1265-4044-a22d-1f2502cb3f22)


- Selanjutnya, unduh dan tambahkan kunci gpg bertanda tangan HashiCorp ke sistem :

         curl -fsSL https://apt.releases.hashicorp.com/gpg | apt-key add -

  ![2](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/ed6384ca-17da-4cbb-b178-94c29d9f1d2c)


- Selanjutnya, tambahkan repositori HashiCorp ke APT menggunakan perintah berikut :

           apt-add-repository "deb [arch=$(dpkg --print-architecture)] https://apt.releases.hashicorp.com $(lsb_release -cs) main"

- Selanjutnya, perbarui repositori :

      apt-get update -y

- Terakhir, Install terraform dengan menjalankan perintah berikut :

      apt-get install terraform -y

![3](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/426cbac8-c07c-4ac2-8589-6b89f86046e1)


- Cek terraform yang berjalan :

      terraform -v

- buat dan edit sesuai kebutuhan terraform script untuk semua pembuatan server

            terraform {
           required_providers {
             idcloudhost = {
               source = "bapung/idcloudhost"
               version = "0.1.3"
             }
           }
         }
         
         provider "idcloudhost" {
             auth_token = "" # API Token from idcloudhost.com
             region = "jkt03"
         }
         
         resource "idcloudhost_vm" "ilham-appserver" {
             name = "ilham-appserver"
             os_name = "ubuntu"
             os_version= "20.04"
             disks = 20
             vcpu = 1
             memory = 1024
             username = "ilham-appserver"
             initial_password = "" # Combination of Uppercase, Lowercase & Numbers
             billing_account_id =  # Billing ID from idcloudhost.com
             public_key = "" # SSH public key
             backup = false
         }
         
         resource "idcloudhost_vm" "ilham-gateway" {
             name = "ilham-gateway"
             os_name = "ubuntu"
             os_version= "20.04"
             disks = 20
             vcpu = 1
             memory = 1024
             username = "ilham-gateway"
             initial_password = "" # Combination of Uppercase, Lowercase & Numbers
             billing_account_id =  # Billing ID from idcloudhost.com
             public_key = "" # SSH public key
             backup = false
         }
         
         resource "idcloudhost_vm" "ilham-monitoring" {
             name = "ilham-monitoring"
             os_name = "ubuntu"
             os_version= "20.04"
             disks = 20
             vcpu = 2
             memory = 2048
             username = "ilham-monitoring"
             initial_password = "" # Combination of Uppercase, Lowercase & Numbers
             billing_account_id =  # Billing ID from idcloudhost.com
             public_key = "" # SSH public key
             backup = false
         }
         
         resource "idcloudhost_floating_ip" "ip-ilham-appserver" {
             name = "ilham-appserver"
             billing_account_id = # Billing ID from idcloudhost.com
             assigned_to = idcloudhost_vm.ilham-appserver.id
         }
         
         resource "idcloudhost_floating_ip" "ip-ilham-gateway" {
             name = "ilham-gateway"
             billing_account_id = # Billing ID from idcloudhost.com
             assigned_to = idcloudhost_vm.ilham-gateway.id
         }

         resource "idcloudhost_floating_ip" "ip-ilham-monitoring" {
             name = "ilham-monitoring"
             billing_account_id =   # Billing ID from idcloudhost.com
             assigned_to = idcloudhost_vm.ilham-monitoring.id
         }

![5](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/cdb5a656-d4cc-49b0-9492-ce8c62360f02)


- Untuk melihat rencana eksekusi Terraform sebelum benar-benar menerapkan perubahan di local, Jalankan perintah :

       terraform init

![4](https://github.com/Hammmzl/devops17-dumbways-MuhammadIlham/assets/96168418/442856dc-d2cb-4cf4-99c4-eb5f62ff3c4d)


- Selanjutnya, untuk menerapkannya gunakan perintah :

       terraform apply

