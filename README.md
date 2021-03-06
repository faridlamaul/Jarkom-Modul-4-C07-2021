# Jarkom-Modul-4-C07-2021

Kelompok C07

|      NRP       |                  Nama                   |
| :------------: | :-------------------------------------: |
| 05111940000046 |       Titian Pamungkas Anjasmara        |
| 05111940000134 |           Ahmad Lamaul Farid            |
| 05111940000150 | Jonathan Leonardo Hasiholan Simanjuntak |

# CPT - VLSM

Pertama - tama, bagi topologi yang sudah diberikan ke dalam beberapa subnet kecil sesuai kebutuhan :

![1.1](images/1.1.png)

Tentukan jumlah IP yang diperlukan beserta dengan netmasknya untuk setiap subnet yang ada :

|  Subnet   | Jumlah IP | Netmask |
| :-------: | :-------: | :-----: |
|    A1     |    701    |   /22   |
|    A2     |   1001    |   /22   |
|    A3     |     2     |   /30   |
|    A4     |     2     |   /30   |
|    A5     |     2     |   /30   |
|    A6     |    101    |   /25   |
|    A7     |   2021    |   /21   |
|    A8     |    521    |   /22   |
|    A9     |     2     |   /30   |
|    A10    |    502    |   /23   |
|    A11    |    13     |   /28   |
|    A12    |     2     |   /30   |
|    A13    |     2     |   /30   |
|    A14    |    721    |   /22   |
|    A15    |    252    |   /24   |
| **Total** | **5845**  | **/19** |

Berdasarkan data tersebut, susun tree subnet VLSM seperti berikut :

![1.2](images/1.2.png)

Dengan demikian, didapatkan NID untuk masing - masing subnet sebagai berikut :

|  Subnet   | Jumlah IP | Netmask |      NID      |
| :-------: | :-------: | :-----: | :-----------: |
|    A1     |    701    |   /22   |  192.187.4.0  |
|    A2     |   1001    |   /22   |  192.187.8.0  |
|    A3     |     2     |   /30   |  192.187.0.0  |
|    A4     |     2     |   /30   |  192.187.0.4  |
|    A5     |     2     |   /30   |  192.187.0.8  |
|    A6     |    101    |   /25   | 192.187.0.128 |
|    A7     |   2021    |   /21   | 192.187.24.0  |
|    A8     |    521    |   /22   | 192.187.12.0  |
|    A9     |     2     |   /30   | 192.187.0.12  |
|    A10    |    502    |   /23   |  192.187.2.0  |
|    A11    |    13     |   /28   | 192.187.0.48  |
|    A12    |     2     |   /30   | 192.187.0.16  |
|    A13    |     2     |   /30   | 192.187.0.20  |
|    A14    |    721    |   /22   | 192.187.16.0  |
|    A15    |    252    |   /24   |  192.187.1.0  |
| **Total** | **5845**  | **/19** |

Masing - masing interface pada sebuah subnet dapat diberikan IP sesuai dengan aturan yang telah diberikan di atas.

- Foosha

![image](https://user-images.githubusercontent.com/77373958/143667818-0d8d7893-0b1e-4564-98b1-49ee0d8aea69.png)

```
IP 192.187.8.1
Subnet Mask 255.255.252.0  // Menuju Blueno
```
```
IP 192.187.0.13
Subnet Mask 255.255.255.252  // Menuju Guanhao
```
```
IP 192.187.0.1
Subnet Mask 255.255.255.252  // Menuju Water7
```
```
IP 192.187.0.9
Subnet Mask 255.255.255.252  // Menuju Doriki
```

- Water 7

![image](https://user-images.githubusercontent.com/77373958/143667832-bd6328b4-07c9-4ab4-b37a-633c76f4d18f.png)

```
IP 192.187.4.1
Subnet Mask 255.255.252.0  // Menuju Chiper
```
```
IP 192.187.0.5
Subnet Mask 255.255.255.252  // Menuju Pucci
```
```
IP 192.187.0.2
Subnet Mask 255.255.255.252  // Menuju Foosha
```

- Pucci

![image](https://user-images.githubusercontent.com/77373958/143667889-39a1190b-20e0-4bb7-bf4d-3dbdb32fa877.png)

```
IP 192.187.0.6
Subnet Mask 255.255.255.252  // Menuju Water7
```
```
IP 192.187.0.129
Subnet Mask 255.255.255.128  // Menuju Jipangu
```
```
IP 192.187.24.1
Subnet Mask 255.255.248.0  // Menuju Cambelt dan Courtyard
```

- Guanhao

![image](https://user-images.githubusercontent.com/77373958/143667910-43220235-d3a0-47f9-aeaf-77d8e071432c.png)

```
IP 192.187.0.14
Subnet Mask 255.255.255.252  // Menuju Foosha
```
```
IP 192.187.2.0
Subnet Mask 255.255.254.0  // Menuju Maingate dan Alabasta
```
```
IP 192.187.12.1
Subnet Mask 255.255.252.0  // Menuju Jabra
```
```
IP 192.187.0.17
Subnet Mask 255.255.255.252  // Menuju Oimo
```

- Alabasta

![image](https://user-images.githubusercontent.com/77373958/143667922-75dbbf4c-f3ba-4a81-98a1-9a1ee57d8abe.png)

```
IP 192.187.2.3
Subnet Mask 255.255.254.0  // Menuju Maingate dan Gunhao
```
```
IP 192.187.0.49
Subnet Mask 255.255.255.240  // Menuju Jorge
```

- Oimo

![image](https://user-images.githubusercontent.com/77373958/143667933-878ea3a4-abc7-47bf-adbc-5e376366b480.png)

```
IP 192.187.0.18
Subnet Mask 255.255.255.252  // Menuju Gunhao
```
```
IP 192.187.0.21
Subnet Mask 255.255.255.252  // Menuju Fukuro
```
```
IP 192.187.1.1
Subnet Mask 255.255.255.0  // Menuju Seastone dan Enies lobby
```

- Seastone

![image](https://user-images.githubusercontent.com/77373958/143667949-19972eec-60f2-4ec4-b533-da6146a31874.png)

```
IP 192.187.1.2
Subnet Mask 255.255.255.0  // Menuju Oimo dan Enies lobby
```
```
IP 192.187.16.1
Subnet Mask 255.255.252.0  // Menuju Elena
```

- Host

![image](https://user-images.githubusercontent.com/77373958/143667958-a005aac4-c466-490a-b4a7-b989fbab4af8.png)

```
IP 192.187.8.2
Subnet Mask 255.255.252.0  // di Blueno
```
```
IP 192.187.4.2
Subnet Mask 255.255.252.0  // di Chiper
```
```
IP 192.187.0.130
Subnet Mask 255.255.255.128  // di Jipangu
```
```
IP 192.187.24.3
Subnet Mask 255.255.248.0  // di Courtyard
```
```
IP 192.187.24.2
Subnet Mask 255.255.248.0  // di Calmbelt
```
```
IP 192.187.12.2
Subnet Mask 255.255.252.0  // di Jabra
```
```
IP 192.187.2.2
Subnet Mask 255.255.254.0  // di Maingate
```
```
IP 192.187.0.50
Subnet Mask 255.255.255.240 // di Jorge
```
```
IP 192.187.16.2
Subnet Mask 255.255.252.0  // di Elena
```
```
IP 192.187.1.3
Subnet Mask 255.255.255.0  // di Enies lobby
```
```
IP 192.187.0.10
Subnet Mask 255.255.255.252  // di Doriki
```
```
IP 192.187.0.22
Subnet Mask 255.255.255.252  // di Fukuro
```


## Routing

Pada kasus topologi yang sudah kami buat ini, route table yang ada pada masing - masing router adalah sebagai berikut :

- PUCCI
  ![1.3](images/1.3-Pucci.png)

- Water7
  ![1.4](images/1.4-Water7.png)

- Foosha
  ![1.5](images/1.5-Foosha.png)

  ![1.6](images/1.6-Foosha.png)

  ![1.7](images/1.7-Foosha.png)

- Guanhao
  ![1.8](images/1.8-Guanhao.png)

- Alabasta
  ![1.9](images/1.9-Alabasta.png)

- Oimo
  ![1.10](images/1.10-Oimo.png)

- Seastone
  ![1.11](images/1.11-Seastone.png)

## Testing

Berikut adalah beberapa testing ping yang dilakukan :

![testing1](images/testing1.PNG)

![testing2](images/testing2.PNG)

![testing3](images/testing3.PNG)

# GNS3 - CIDR

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

## Testing

Lakukan ping antar node atau ke jaringan luar. Disini kami menggunakan `ping youtube.com` dengan testing nodenya `Fukurou`. Jika semua routing kita sudah benar maka kita dapat melakukan `ping` seperti pada gambar berikut :

![2.27](images/2.27.png)

_PS : Pastikan semua node dapat melakukan ping seperti gambar diatas_
