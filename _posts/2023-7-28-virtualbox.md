---
layout: post
title: installasi virtualbox
---

## Pengertian

Virtualbox adalah salah satu perangkat lunak virtualisasi untuk menginstall sistem operasi "operasi system" . kata virtualisasi

yaitu mengubah atau mengkonversi sesuatu dari bentuk real menjadi bentuk simulasi. apabila anda ingin tahun lebih jauh sejarah 

dan pengertian dari vritualbox anda bisa mengujungi link berikut

[sumber virtualbox](https://barki.uma.ac.id/2022/01/04/pengertian-sejarah-fungsi-dan-manfaat-virtualbox/)

baik di sini saya akan mengasih tutorial menginstall virtualbox dengan 2 opsi yaitu

### Opsi 1 install virtualbox dari repositori Ubuntu

> ctrl+alt+T untuk membuka terminal

**lalu anda bisa menjalankan perintah seperti berikut**

```bash
sudo apt-get update
```
**lalu install virtual box**

```bash
sudo apt-get install virtualbox
```

**selanjutnya instaall paket extensi virtualbox**

```bash
sudo apt-get install virtualbox—ext–pack
```

Baca Lisensi Penggunaan Pribadi dan Evaluasi VirtualBox Extension Pack dan pilih <Ok> untuk mengonfirmasi bahwa Anda mengerti

lalu klik **<yes>** dan tekan __Enter__ untuk mengakhiri installasi. lalu akan ada output yang menampilkan  Anda telah berhasil

menginstall  Oracle VM VirtualBox Extension Pack.


### Opsi 2 Menginstall virtualbox dari repositoti oracle

Seringkali repositori default tidak memiliki perangkat lunak versi terbaru. Mereka mungkin berfungsi untuk lingkungan pengujian, 

tetapi beberapa pengguna memerlukan tambalan keamanan atau fungsionalitas terbaru. Proses ini lebih mendalam tetapi menginstal 

versi terbaru dari VirtualBox di Ubuntu.

**Instal perangkat lunak Pendukung**

Paket software-properties-commondiperlukan untuk menjalankan Virtualbox di Ubuntu. Ini memungkinkan Anda untuk menambahkan 

repositori perangkat lunak baru. ketikan perintah berikut

```bash
sudo apt-get install software–properties–common
```

**Instal kunci GPG**

Kunci GPG memungkinkan Anda memverifikasi dan berkomunikasi dengan repositori VirtualBox.

Untuk mengunduh dan menginstal kunci GPG, gunakan perintah:

```bash
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add –
```

**Tambahkan Repositori VirtualBox ke Ubuntu**

Untuk menambahkan repositori VirtualBox, masukkan perintah:

```bash
echo "deb [arch=amd64] http://virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list
```

**Instal Versi Terbaru dari VirtualBox**

1. mulai dengan memperbarui daftar paket

   ```bash
   sudo apt-get update
   ```

2. Untuk Install VirtualBox 7.0 di Ubuntu, gunakan perintah berikut

```bash
sudo apt-get install virtualbox–7.0
```

Pada saat nulis artikel ini versi paling terbaru dari virtualbox adalah versi 7.0 dan itu mendukung untuk sistem operasi 64-bit

 **Instal Paket Ekstensi VirtualBox**

Paket Ekstensi VirtualBox meningkatkan fungsionalitas mesin virtual Anda. Itu menambahkan alat tambahan seperti USB 2.0 dan 3.0, 

Remote Desktop, dan enkripsi. 

1.ketikan perintah seperti berikut

```bash
wget https://download.virtualbox.org/virtualbox/6.1.26/Oracle_VM_VirtualBox_Extension_Pack-6.1.26.vbox-extpack
```

2. perintah seperti berikut

```bash

sudo VBoxManage extpack install Oracle_VM_VirtualBox_Extension_Pack-7.0.10.vbox-extpack
```


konfirmasikan penginstalan, lalu biarkan proses selesai


























