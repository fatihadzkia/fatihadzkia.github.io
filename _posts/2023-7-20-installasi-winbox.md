---
layout: post
title:  installasi winbox di ubuntu
---

Di sini saya akan memberi tutorian meng install winbox di OS Ubuntu yang sebagaimna kita tahu winbox adalah aplikasi yang biasanya
berjalan di OS windows tapi bukan berarti tidak bisa berjalan di linux

### Installasi Wine

sebagai pemecah masalah untuk menjalankan apk yang berbasis windows di linux kita bisa menggunakan wine

pertama kita bisa masuk ke daalam root terlebih dahulu

```bash
$ sudo su
```

setelah masuk ke root kita bisa meng install wine dengan 2 cara yaitu apt-get install wine atau dengan apt-get install wine-stable

di sini saya akan menggunakan apt-get install wine

```bash
# apt-get install wine
```

tunggu hingga proses install wine selesai

### Installasi winbox

setelah anda berhasil menginstall wine anda juga harus mengisntall winbox terlebih dahulu [disini](https://mikrotik.com/download)


![winbox4]({{ site.baseurl }}/images/wb4.png)

klik tombol winbox untuk mengunduh file **.exe** versi terbaru. setelah unduhan selesai anda anda bisa menaruh file winbox di 

di drektori yang mudah anda akses

file **winbox.exe** ini bukan merupakan file paket instalasi melaikan file launcher jadi anda tidak perlu melakukan installasi 

lagi untuk menjalankan winbox 

untuk menjalan kan winbox anda bisa menjalankan perintah di bawah ini 

```bash
# winebox.exe
```

> pastikan anda menjalankan perintah di atas di direktori tempat file winbox.exe berada

sourc:
[sumber1](https://www.excellentcom.id/cara-install-winbox-di-linux-ubuntu/)
[sumber2](https://bandithijo.dev/blog/instal-dan-konfigurasi-winbox-linux)










