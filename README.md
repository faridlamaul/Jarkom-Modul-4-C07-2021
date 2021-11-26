# Jarkom-Modul-4-C07-2021

Kelompok C07

|      NRP       |                  Nama                   |
| :------------: | :-------------------------------------: |
| 05111940000046 |       Titian Pamungkas Anjasmara        |
| 05111940000134 |           Ahmad Lamaul Farid            |
| 05111940000150 | Jonathan Leonardo Hasiholan Simanjuntak |

**CPT - VLSM**

**GNS3 - CIDR**

Pembagian subnet di CIDR dimulai dari yang terjauh dari cloud agar mempermudah routing sehingga didapatkan subnet sebagai berikut :

![2.1](images/2.1.png)

Dari gambar diatas dapat kita buat tree subnet CIDR seperti berikut :

![2.2](images/2.2.png)

| Subnet | Jumlah IP | Netmask |      NID      |
| :----: | :-------: | :-----: | :-----------: |
|   A1   |    701    |   /22   | 192.187.32.0  |
|   A2   |   1001    |   /22   | 192.187.128.0 |
|   A3   |     2     |   /30   | 192.187.64.0  |
|   A4   |     2     |   /30   | 192.187.16.0  |
|   A5   |     2     |   /30   | 192.188.64.0  |
|   A6   |    101    |   /25   |  192.187.8.0  |
|   A7   |   2021    |   /21   |  192.187.0.0  |
|   A8   |    521    |   /22   | 192.188.20.0  |
|   A9   |     2     |   /30   | 192.188.32.0  |
|  A10   |    502    |   /23   | 192.188.16.0  |
|  A11   |    13     |   /28   | 192.188.18.0  |
|  A12   |     2     |   /30   | 192.188.24.0  |
|  A13   |     2     |   /30   |  192.188.8.0  |
|  A14   |    721    |   /22   |  192.188.0.0  |
|  A15   |    252    |   /24   |  192.188.4.0  |

Kemudian buat topologi pada GNS3 seperti berikut :

![topologi-gns3](images/topologi-gns3.png)

Untuk configurasi pada topologi GNS3 diatas sebagai berikut :

![2.3](images/2.3.png)

![2.4](images/2.4.png)

![2.5](images/2.5.png)

![2.6](images/2.6.png)

![2.7](images/2.7.png)

![2.8](images/2.8.png)

![2.9](images/2.9.png)

![2.10](images/2.10.png)

![2.11](images/2.11.png)

![2.12](images/2.12.png)

![2.13](images/2.13.png)

![2.14](images/2.14.png)

![2.15](images/2.15.png)

![2.16](images/2.16.png)

![2.17](images/2.17.png)

![2.18](images/2.18.png)

![2.19](images/2.19.png)

![2.20](images/2.20.png)

![2.21](images/2.21.png)

![2.22](images/2.22.png)

Setelah melakukan configurasi seperti gambar diatas, maka langkah selanjutnya adalah routing. Untuk routingnya dilakukan pada node Foosha, Water7, Guanhao, Oimo seperti pada gambar berikut :

![2.23](images/2.23.png)

![2.24](images/2.24.png)

![2.25](images/2.25.png)

![2.26](images/2.26.png)

Ketikkan perintah `echo nameserver 192.168.122.1 > /etc/resolv.conf` pada setiap node yang ada di topologi GNS3 agar semua node dapat mengakses internet

**Testing**

Lakukan ping antar node atau ke jaringan luar. Disini kami menggunakan `ping youtube.com` dengan testing nodenya `Fukurou`. Jika semua routing kita sudah benar maka kita dapat melakukan `ping` seperti pada gambar berikut :

![2.27](images/2.27.png)

_PS : Pastikan semua node dapat melakukan ping seperti gambar diatas_
