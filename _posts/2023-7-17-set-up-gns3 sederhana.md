---
layout: post
title: set up GNS3 sederhana
---
### installasi
anda bisa mengikuti command line di bawah ini untk installasi GNS3 di Ubuntu 64-bit 

```bash
# sudo add-apt-repository ppa:gns3/ppa
# sudo apt update
# sudo apt install gns3-gui gns3-server
```
berikutnya apabila di kernel ubuntu anda ada docker versi lama maka hapus terlebih dahulu

```bash
# sudo apt remove docker docker-engine docker.io
```
install paket paket berikut ini 

```bash 
# sudo apt-get install apt-transport-https ca-certificates curl \ software-properties-common
```

import gpkg key docker seperti perintah di bawah

```bash
# curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
tambahkan repositori yang sesuai

```bash
# sudo add-apt-repository \
"deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) stable"
```
kemudian install docker kembali

```bash
# sudo apt update
# sudo apt install docker-ce
```
##
lalu yang terakhir masukan user anda ke dalam grup dengan perintah di bawah ini 

```bash
# sudo usermod -aG ubridge libvirt kvm wireshark docker $USER
```
setelah itu lakukan relog pada user linux anda

### instalasi mikrotik 

pertama tama anda harus menginstall dengan mengabil file mikrotik di mikrotik.com


