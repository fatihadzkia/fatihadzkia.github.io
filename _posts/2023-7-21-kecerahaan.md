---
laayou: post
title: tutorial mengatur kecerahan manual di linux
---

### hanya untuk orang yang menyusahkan diri

masuk root terlebih dahulu
```bash
sudo su
```
lalu ketikan perintah sebagai berikut
```bash
echo 2100 > /sys/class/backlight/intel_backlight/brightness
```
> nominal angka bisa di ganti sesuai kebutuhan 

untuk mempermudah anda bisa mengakali nya dengan shell script sebagai berikut

```bash
read -p "Masukan angka untuk tingkatan pencahayaan:(1800-5000) " light
if ((light >= 1800 && light <= 5000)); then
        echo $light > /sys/class/backlight/intel_backlight/brightness
        echo "Pencahayaan telah di set"
else
        echo "angka yang anda masukan tidak valid"
fi
```
