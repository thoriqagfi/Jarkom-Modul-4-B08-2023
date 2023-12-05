# Praktikum Jarkom Modul 4

|Nama|NRP|Kelas|
|:--:|:-:|:---:|
|Adrian Karuna Soetikno|5025211019|Jarkom B|
|Thariq Agfi Hermawan|5025211215|Jarkom B|
------------------------------------------



## VLSM 
------------------------------------------------------------------------------------------------

### Topologi VLSM (GNS3)

<img width="1376" alt="Screenshot 2023-12-05 at 11 15 07" src="https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/86884506/63f79794-e890-47d1-b75f-b588713e2829">

### Tree VLSM

![1](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/86884506/0b429488-b701-4c3d-b18e-31afcbe61fd7)

link : https://www.canva.com/design/DAF1pfKjvRw/wUlrzshVWHUEDNRMNEcx_Q/edit?utm_content=DAF1pfKjvRw&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

### Pembagian Rute VLSM

<img width="640" alt="Screenshot 2023-12-05 at 11 22 50" src="https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/86884506/c2995821-c431-40a9-9b4d-b6aa6cd878b1">

### Pembagian IP

<img width="573" alt="Screenshot 2023-12-05 at 11 23 30" src="https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/86884506/062fc973-d764-430b-a5b8-7a7641ed1670">

### Konfigurasi Tiap Node : 

#### A1 (Apetit Region)
```
auto eth0
iface eth0 inet static
address 192.182.24.2
netmask 255.255.248.0
gateway 192.182.24.1
```

#### A1 (LaubHills)
```
auto eth0
iface eth0 inet static
address 192.182.24.3
netmask 255.255.248.0
gateway 192.182.24.1
```

#### A2 (RorhRoad 1000 host)
```
auto eth0
iface eth0 inet static
address 192.182.4.2
netmask 255.255.252.0
gateway 192.182.4.1
```

#### A3 (SchwerMountains 5 host)
```
auto eth0
iface eth0 inet static
address 192.182.0.50
netmask 255.255.255.248
gateway 192.182.0.48
```

#### Fern (A1, A4)
```
auto lo
iface lo inet loopback
auto eth0
iface eth0 inet static
address 192.182.0.2
netmask 255.255.255.252
gateway 192.182.0.1
auto eth1
iface eth1 inet static
address 192.182.24.1
netmask 255.255.248.0
```

#### Flamme (A4, A5, A6)
```
auto lo
iface lo inet loopback
auto eth0
iface eth0 inet static
address 192.182.0.10
netmask 255.255.255.252
gateway 192.182.0.9
auto eth1
iface eth1 inet static
address 192.182.0.1
netmask 255.255.255.252
auto eth2
iface eth2 inet static
address 192.182.0.5
netmask 255.255.255.252
auto eth3
iface eth3 inet static
address 192.182.4.1
netmask 255.255.252.0
```

#### Himmel (A5, A3)
```
auto lo
iface lo inet loopback
auto eth0
iface eth0 inet static
address 192.182.0.6
netmask 255.255.255.252
gateway 192.182.0.5
auto eth1
iface eth1 inet static
address 192.182.0.49
netmask 255.255.252.248
```

#### Aura
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp

auto eth1 #ke denken
iface eth1 inet static
address 192.182.0.29
netmask 255.255.255.252

auto eth2 #Ke Frieren
iface eth2 inet static
address 192.182.0.13
netmask 255.255.255.252

auto eth3 #ke Eisen
iface eth3 inet static
address 192.182.0.21
netmask 255.255.255.252
```

#### Stark (A17)
```
auto eth0 #ke Eisen
iface eth0 inet static
address 192.182.0.34
netmask 255.255.255.252
gateway 192.182.0.33
```

#### A9 (Richter Revolte)
```
auto eth0 #ke Eisen
iface eth0 inet static
address 192.182.0.58
netmask 255.255.255.248
gateway 192.182.0.57
```

#### Revolte
```
auto eth0 #ke Eisen
iface eth0 inet static
address 192.182.0.59
netmask 255.255.255.248
gateway 192.182.0.57
```

#### Frieren

```
auto lo
iface lo inet loopback
auto eth0 #ke aura
iface eth0 inet static
address 192.182.0.14
netmask 255.255.255.252
gateway 192.182.0.13
auto eth1 #ke Flamme
iface eth1 inet static
address 192.182.0.9
netmask 255.255.255.252
auto eth2 #Ke Lakecorridor
iface eth2 inet static
address 192.182.0.129
netmask 255.255.255.224
```

#### Eisen
```
auto lo
iface lo inet loopback
auto eth0 #ke Aura
iface eth0 inet static
address 192.182.0.22
netmask 255.255.255.252
gateway 192.182.0.21

auto eth1 #ke Linie
iface eth1 inet static
address 192.182.0.25
netmask 255.255.255.252

auto eth2 #ke Lugner
iface eth2 inet static
address 192.182.0.37
netmask 255.255.255.252

auto eth3 #ke Stark
iface eth3 inet static
address 192.182.0.33
netmask 255.255.255.252

auto eth4 #ke Switch11
iface eth4 inet static
address 192.182.0.57
netmask 255.255.255.248
```

#### Denken
```
auto lo
iface lo inet loopback

auto eth0 #ke aura
iface eth0 inet static
address 192.182.0.30
netmask 255.255.255.252
gateway 192.182.0.29

auto eth1 #ke ke Royal dan wille
iface eth1 inet static
address 192.182.2.1
netmask 255.255.255.0
```

#### Royal Capital
```
auto eth0 #ke Denken
iface eth0 inet static
address 192.182.2.2
netmask 255.255.255.0
gateway 192.182.2.1
```

#### Wille Region
```
auto eth0 #ke Denken
iface eth0 inet static
address 192.182.2.3
netmask 255.255.255.0
gateway 192.182.2.1
```

#### Linie
```
auto lo
iface lo inet loopback
auto eth0 #ke Eisen
iface eth0 inet static
address 192.182.0.26
netmask 255.255.255.252
gateway 192.182.0.25

auto eth1 #ke Lawine
iface eth1 inet static
address 192.182.0.17
netmask 255.255.255.252

auto eth2 #keGranz
iface eth2 inet static
address 192.182.16.1
netmask 255.255.254.0
```

#### Lugner
```
auto lo
iface lo inet loopback
auto eth0 #ke Eisen
iface eth0 inet static
address 192.182.0.38
netmask 255.255.255.252
gateway 192.182.0.37

auto eth1 #ke TurkRegion
iface eth1 inet static
address 192.182.12.1
netmask 255.255.252.0

auto eth2 #keGrobe
iface eth2 inet static
address 192.182.3.1
netmask 255.255.255.0
```

#### Turk Region (A20)
```
auto eth0 # ke lugner
iface eth0 inet static
address 192.182.12.2
netmask 255.255.252.0
gateway 192.182.12.1
```

#### Grobe Forest (A21)
```
auto eth0 # ke lugner
iface eth0 inet static
address 192.182.3.2
netmask 255.255.255.0
gateway 192.182.3.1
```

#### Granz (A15)
```
auto eth0 #ke Linie
iface eth0 inet static
address 192.182.16.2
netmask 255.255.254.0
gateway 192.182.16.1
```

#### Lawine (A12)
```
auto lo
iface lo inet loopback
auto eth0 #ke Linie
iface eth0 inet static
address 192.182.0.18
netmask 255.255.255.252
gateway 192.182.0.17

auto eth1 #ke Sw7 (A10)
iface eth1 inet static
address 192.182.0.65
netmask 255.255.252.192
```

#### Bredt Region (A10)
```
auto eth0 #ke Lawine
iface eth0 inet static
address 192.182.0.66
netmask 255.255.255.192
gateway 192.182.0.65
```

#### Heiter (A10,A11)
```
auto lo
iface lo inet loopback
auto eth0 #ke Lawine
iface eth0 inet static
address 192.182.0.67
netmask 255.255.255.192
gateway 192.182.0.65

auto eth1 #ke A11
iface eth1 inet static
address 192.182.8.1
netmask 255.255.252.0
```

#### SEIN
```
auto eth0 #ke Heiter
iface eth0 inet static
address 192.182.8.2
netmask 255.255.252.0
gateway 192.182.8.1
```

#### RIEGEL
```
auto eth0 #ke Heiter
iface eth0 inet static
address 192.182.8.3
netmask 255.255.252.0
gateway 192.182.8.1
```

### Routing Routers

#### Fern
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 192.182.24.0 netmask 255.255.248.0 gw 192.182.24.1
```
#### Flamme
```
echo nameserver 192.168.122.1 > /etc/resolv.conf

#fern
route add -net 192.182.24.0 netmask 255.255.248.0 gw 192.182.0.2
route add -net 192.182.0.0 netmask 255.255.255.252 gw 192.182.0.2

#Himmel
route add -net 192.182.0.48 netmask 255.255.255.248 gw 192.182.0.6
route add -net 192.182.0.4 netmask 255.255.255.252 gw 192.182.0.6

#kiri 
route add -net 192.182.4.0 netmask 255.255.252.0 gw 192.182.4.1
```

#### Himmel
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 192.182.0.48 netmask 255.255.255.248 gw 192.182.0.49
```

#### Frieren
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 192.182.24.0 netmask 255.255.248.0 gw 192.182.0.10
route add -net 192.182.4.0 netmask 255.255.252.0 gw 192.182.0.10
route add -net 192.182.0.48 netmask 255.255.255.248 gw 192.182.0.10
route add -net 192.182.0.0 netmask 255.255.255.252 gw 192.182.0.10
route add -net 192.182.0.4 netmask 255.255.255.252 gw 192.182.0.10
route add -net 192.182.0.8 netmask 255.255.255.252 gw 192.182.0.10
route add -net 192.182.0.128 netmask 255.255.255.224 gw 192.182.0.129
```

#### Aura
```
iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.182.0.0/16
#denkens
route add -net 192.182.0.28 netmask 255.255.255.252 gw 192.182.0.30
route add -net 192.182.2.0 netmask 255.255.255.0 gw 192.182.0.30

#frieren
route add -net 192.182.0.4 netmask 255.255.255.252 gw 192.182.0.14
route add -net 192.182.0.8 netmask 255.255.255.252 gw 192.182.0.14
route add -net 192.182.24.0 netmask 255.255.248.0 gw 192.182.0.14
route add -net 192.182.4.0 netmask 255.255.252.0 gw 192.182.0.14
route add -net 192.182.0.48 netmask 255.255.255.248 gw 192.182.0.14
route add -net 192.182.0.12 netmask 255.255.255.252 gw 192.182.0.14
route add -net 192.182.0.128 netmask 255.255.255.224 gw 192.182.0.14
route add -net 192.182.0.0 netmask 255.255.255.252 gw 192.182.0.14

#Eisen
#A13
route add -net 192.182.0.20 netmask 255.255.255.252 gw 192.182.0.22
#A29,A17
route add -net 192.182.0.56 netmask 255.255.255.248 gw 192.182.0.22
route add -net 192.182.0.32 netmask 255.255.255.252 gw 192.182.0.22
#A18-21
route add -net 192.182.0.36 netmask 255.255.255.252 gw 192.182.0.22
route add -net 192.182.12.0 netmask 255.255.252.0 gw 192.182.0.22
route add -net 192.182.3.0 netmask 255.255.255.0 gw 192.182.0.22
#A14-15
route add -net 192.182.0.24 netmask 255.255.255.252 gw 192.182.0.22
route add -net 192.182.16.0 netmask 255.255.254.0 gw 192.182.0.22
route add -net 192.182.0.64 netmask 255.255.255.192 gw 192.182.0.22
route add -net 192.182.8.0 netmask 255.255.252.0 gw 192.182.0.22
route add -net 192.182.0.16 netmask 255.255.255.252 gw 192.182.0.22
```

#### Denken
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.182.0.29
```

#### Eisen
```
echo nameserver 192.168.122.1 > /etc/resolv.conf

#A17
route add -net 192.182.0.32 netmask 255.255.255.252 gw 192.182.0.33
#A9
route add -net 192.182.0.56 netmask 255.255.255.248 gw 192.182.0.57
#18,20,21
route add -net 192.182.0.36 netmask 255.255.255.252 gw 192.182.0.38
route add -net 192.182.12.0 netmask 255.255.252.0 gw 192.182.0.38
route add -net 192.182.3.0 netmask 255.255.255.0 gw 192.182.0.38
#14-15
route add -net 192.182.0.24 netmask 255.255.255.252 gw 192.182.0.26
route add -net 192.182.16.0 netmask 255.255.254.0 gw 192.182.0.26
#10-12
route add -net 192.182.0.64 netmask 255.255.255.192 gw 192.182.0.26
route add -net 192.182.8.0 netmask 255.255.252.0 gw 192.182.0.26
route add -net 192.182.0.16 netmask 255.255.255.252 gw 192.182.0.26
```

#### Lugner
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 192.182.12.0 netmask 255.255.252.0 gw 192.182.12.1
route add -net 192.182.3.0 netmask 255.255.255.0 gw 192.182.3.1
```

#### Linie
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
#10-12
route add -net 192.182.0.64 netmask 255.255.255.192 gw 192.182.0.18
route add -net 192.182.8.0 netmask 255.255.252.0 gw 192.182.0.18
route add -net 192.182.0.16 netmask 255.255.255.252 gw 192.182.0.18
#A15 granz
route add -net 192.182.16.0 netmask 255.255.254.0 gw 192.182.16.1
```

#### Lawine
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 192.182.0.64 netmask 255.255.255.192 gw 192.182.0.65
route add -net 192.182.8.0 netmask 255.255.252.0 gw 192.182.0.67
```

#### Heiter
```
echo nameserver 192.168.122.1 > /etc/resolv.conf
route add -net 192.182.8.0 netmask 255.255.252.0 gw 192.182.8.1
```

## CIDR
------------------------------------------------------------------------------------------------

[Sheets Pembagian Rute dan IP](https://docs.google.com/spreadsheets/d/1gP3S17p5vlYtttezMkZ4iXBQzFwZOKPBHgAlXtQQ--M/edit?usp=sharing)

### Topologi PKT CIDR

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/274c99bc-7de9-440e-9f1c-19ade2f6b2cb)

### Subnetting Rute CIDR

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/35cb7830-88a0-4b1c-86f3-18075fe41c0d)

Diatas adalah pembagian subnetting metode CIDR.
Untuk membuat subnetting, pertama kita buat seluruh koneksi antar router dan client
![Jarkom CIDR - Frame 1](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/5c5a8443-1173-4077-965a-b8d97759153a)

Selanjutnya, kita melakukan penggabungan kedua (B) dengan mencari subnet terjauh dari Cloud dan didapatkan hanya 1 subnet terjauh dari Cloud
![Jarkom CIDR - Frame 2](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/c0630e40-c769-4fc2-9aed-8cd1efd3080c)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/682a4fb7-0e58-48b5-a429-d04f58fa6ad6)

Penggabungan 2 (C)
![Jarkom CIDR - Frame 3](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/a08e7941-71f5-4699-bfdd-26b3237362b0)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/0645ac43-a859-4039-b22a-076b8dfae53c)

Penggabungan 3 (D)
![Jarkom CIDR - Frame 4](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/fc3547fe-e315-4e06-a990-f00c351d2b64)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/e65a40cd-74cd-486c-83c5-e2d1a45f0629)

Penggabungan 4 (E)
![Jarkom CIDR - Frame 5](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/6265be94-b9e3-4e60-9cb8-691f4fb89ca3)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/1f1d79cb-1fec-403e-a350-ef249dae18c9)

Penggabungan 5 (F)
![Jarkom CIDR - Frame 6](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/dce164ae-e53d-4392-9bac-b7ca3db5bc49)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/7df519b4-09fd-4fa7-8821-25ceb8a31d0e)

Penggabungan 6 (G)
![Jarkom CIDR - Frame 7](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/8577cb1f-7c42-4a5f-8da4-ca847f4d0c01)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/a6cc2cb0-cf06-4979-9802-c1fd2949da3c)

Penggabungan 7 (H)
![Jarkom CIDR - Frame 8](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/a97e2a4c-a944-4c19-b943-e49fa2d8a0df)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/1d0115be-fe43-4d53-95b4-2628c703f3aa)

Penggabungan 8 (I)
![Jarkom CIDR - Frame 9](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/db348867-fd82-41df-8b05-c25d827197d0)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/686da4ab-0d01-4b78-a698-2269f8607f45)

Penggabungan 9 (J)
![Jarkom CIDR - Frame 10](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/8f06626a-6f3d-4e2f-87ae-e2ea6db19c83)

![image](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/b5fc4c7b-d1bd-418c-9f21-9ba36358a831)

### Tree CIDR

![Jarkom CIDR - Tree CIDR](https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/a4419373-7225-470c-9672-11f9a401b8a8)

### Pembagian IP

### Testing

https://github.com/thoriqagfi/Jarkom-Modul-4-B08-2023/assets/92865110/ff03f4d3-bfb4-41f2-af4b-9fa143d91fad

