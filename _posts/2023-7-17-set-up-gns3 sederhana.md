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

pertama tama anda harus menginstall dengan mengabil img image mikrootik pada sumber ddi bawah ini 

[mikrotik downloaad](https://download.mikrotik.com/routeros/6.49.8/chr-6.49.8.img.zip)

setelah anda mendowload img image pastikan anda juga meng extracx nya terlebih dahulu seperti padagambar di bawah

![qemu0]({{ site.baseurl }}/images/qemu0.png)

setelah anda berhasil meng extracx file nya anda harus membuka gns3 yang sudah kita install sebelum nya

setelah anda masuk ke gns3 anda bisa memilih edit yang berada di bagian atas kiri, lalu pilih preferences 

apabila tampilan sudah seperti pada gambar di bawah ini pilih qemu lalu klik new 

![qemu1]({{ site.baseurl }}/images/qemu1.png)

lalu beri nama contoh seperti pada gambar > untuk nama bisa di sesuiakn dengan kebutuhan anda

![qemu2]({{ site.baseurl }}/images/qemu2.png)

setelah itu klik next apabila sudah muncul seperti pada gambar anda bisa memilih telnet sebagai konsole nya lalu klik next

![qemu3]({{ site.baseurl }}/images/qemu3.png)

setellaah itu pilih new image klik browser untuk mecari sumber img yang sudah kita extract tadi lalu klik finish 

![qemu4]({{ site.baseurl }}/images/qemu4.png)

setelah itu klik edit dan samakan beberapa formmat seperti pada gambar 

![qemu5]({{ site.baseurl }}/images/qemu5.png)

![qemu6]({{ site.baseurl }}/images/qemu6.png)

> pastikan anda sudah menginstall xtrm untuk bisa mejalankan konsole mikrotik di gns3


### membuat topologi singkat di gns3

saya akan membuat topo logi singkat menggunakan Router,Mikrotik,dan beberapa pc client

berikut gambar topologi singkat yang coba saya buat

![topologi1]({{ site.baseurl }}/images/topologi1.png)

setelah topologi selesai anda bisa langsung meng start mikrotik lalu masuk ke bagian console mikrotik anda

setelah itu anda bisa menyeting ip mikrotik anda dengan perintah seperti berikut 

```bash
ip add add address= 192.168.1.1/24 interface= ether2
ip dhcp-client interface= 1
ip add pr
```
 untuk ip address bisa di sesuiakan dengan kebutuhan begitupun dengan interface

di topologi saya ether 1 saya hubungkan ke internet dan ether 2 saya hubungkan ke switch yang nanti nya akan memberikan ip ke pada para pc client 

setelah anda menyeting ip untuk mikrotik selanjutnya anda harus mengsetup dhcp-server dengan perintah sebagai berikut 

```bash
ip dhcp-server setup
```

apabila anda tidak di minta untuk seperti menyeting berapa jumlah cliennt,dns,dll anda bisa langsung mengklik next saja sampai selesai

setelah itu anda bisa mengecek dhcp-server dengan perintah sebagai berikut

```bash
ip dhcp-server print
```

berikut nya anda harus melakukan setup di firewell. untuk di firewell senddiri saya akan menggunakn winbox untuk contoh nya seperti pada gambar di bawah

> jadi pastikan terlebih dahulu anda sudah menginstaal winbox di pc atau laptop anda

![winbox1]({{ site.baseurl }}/images/wb1.png)

lalu anda juga perlu untuk menyeeting di bagian action nya seperti berikut 

![winbox2]({{ site.baseurl }}/images/wb2.png)

setelah selesai menyeting di mkrotik kita akan menyeting di pcc client

untuk pc client vps anda  hanya perlu mengetikan perintah seperti berikut

```bash
ip dhcp
```

setelah itu anda bisa mengecek apabila sudah menjalankan perintah di atas

```
show ip
ping google.com
```
apabila sudah bisa ping google seperti di atas maka pc vps sudah dapat akses internet dan ip dari mikrotik

untuk selajut nya mengecek di clien slax. anda hanya perlu menjalankan slax lalu ke bagian next manager

apabila sudah seperti gambar di bawah maka slax anda sudah mendapatkan internet dan ip secara dinamic dari mikrotik

![winbox3]({{ site.baseurl }}/images/wb3.png)













