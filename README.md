# Jarkom-Modul-4-IT43-2024

### Kelompok IT43 -

| Name                              |     NRP    |
| ----------------------------------|------------|
| Rafael Jonathan Arnoldus          | 5027231006 | 
| Gandhi Ert Julio                  | 5027231081 |

## Topologi

Topologi CPT VLSM
![Foto Topologi](https://github.com/user-attachments/assets/a1536018-67ee-4bf5-9f15-801f09d96e2d)

## Pembagian rute area subnet

| Nama Subnet | Area Subnet                                                                           | Jumlah IP | Netmask |
| ----------- | ------------------------------------------------------------------------------------- | --------- | ------- |
| A1          | Hololive - Holo-EN                                                                    | 2         | /30     |
| A2          | Holo-EN - HoloAdvent                                                                  | 2         | /30     |
| A3          | Holo-EN - Holo-Myth                                                                   | 2         | /30     |
| A4          | Holo-Myth - Switch2 - Gura_Aine_Ina (309 Host) - Kiara_Calli (193 Host)               | 503       | /23     |
| A5          | HoloAdvent - Switch0 - FuwaMoco (5 Host) - Shiori_Nerissa (12 Host) - Biboo (10 Host) | 28        | /27     |
| A6          | Holo-Myth - HoloPromise - Router4 - Holo-Council                                      | 3         | /29     |
| A7          | Router4 - Tys (2 Host)                                                                | 3         | /29     |
| A8          | Holo-Council - Switch4 - Kronii_Mumei (39 Host) - Bae_Fauna (22 Host)                 | 62        | /26     |
| A9          | Hololive - Holo-JP                                                                    | 2         | /30     |
| A10         | Holo-JP - Switch1 - DEV_IS - GEN:0                                                    | 3         | /29     |
| A11         | DEV_IS - `Re:GLO$$` - Ririka_Raden (3 Host) - Ao (3 Host) - Hajime_Kanade (7 Host)    | 14        | /28     |
| A12         | GEN:0 - Switch3 - MiComet (1501 Host) - Sora_Robo_AZKi (542 Host) - GEN:1             | 2045      | /21     |
| A13         | GEN:1 - GAMERS                                                                        | 2         | /30     |
| A14         | GAMERS - Switch13 - Korone (51 Host) - Okayu (32 Host) - Mio (36 Host)                | 120       | /25     |
| A15         | GEN:1 - Member - FBK_Matsuri (321 Host) - Aki_Hachama (148 Host)                      | 470       | /23     |
| A16         | Hololive - Holp-ID                                                                    | 2         | /30     |
| A17         | Holo-ID - AREA15                                                                      | 2         | /30     |
| A18         | AREA15 - Switch6 - Risu (319 Host) - Moona (201 Host) - lofi (140 Host)               | 661       | /22     |
| A19         | Holo-ID - holoro                                                                      | 2         | /30     |
| A20         | Holo-ID - holoh3ro                                                                    | 2         | /30     |
| A21         | holoh3ro - Switch8 - Zeta (81 Host) - Kaela (71 Host) - Kobo (146 Host)               | 299       | /23     |
| A22         | holoro - Switch7 - Ollie (20 Host) - Anya (3 Host) - Reine (10 Host)                  | 34        | /26     |
| Total       |                                                                                       | 4263      | /19     |

# Subnetting

## Subnetting CPT VLSM
### Prefix : 192.238.x.x

| Subnet | Network ID     | Netmask               | Broadcast      | Range IP (Usable)           |
|--------|----------------|-----------------------|----------------|-----------------------------|
| A12    | 192.238.0.0    | 255.255.248.0 (/21)   | 192.238.7.255  | 192.238.0.1 - 192.238.7.254 |
| A18    | 192.238.8.0    | 255.255.252.0 (/22)   | 192.238.11.255 | 192.238.8.1 - 192.238.11.254|
| A15    | 192.238.12.0   | 255.255.254.0 (/23)   | 192.238.13.255 | 192.238.12.1 - 192.238.13.254|
| A21    | 192.238.14.0   | 255.255.254.0 (/23)   | 192.238.15.255 | 192.238.14.1 - 192.238.15.254|
| A4     | 192.238.16.0   | 255.255.254.0 (/23)   | 192.238.17.255 | 192.238.16.1 - 192.238.17.254|
| A8     | 192.238.18.0   | 255.255.255.192 (/26) | 192.238.18.63  | 192.238.18.1 - 192.238.18.62 |
| A22    | 192.238.18.64  | 255.255.255.192 (/26) | 192.238.18.127 | 192.238.18.65 - 192.238.18.126|
| A14    | 192.238.18.128 | 255.255.255.128 (/25) | 192.238.18.255 | 192.238.18.129 - 192.238.18.254|
| A5     | 192.238.19.0   | 255.255.255.224 (/27) | 192.238.19.31  | 192.238.19.1 - 192.238.19.30 |
| A11    | 192.238.19.32  | 255.255.255.240 (/28) | 192.238.19.47  | 192.238.19.33 - 192.238.19.46 |
| A6     | 192.238.19.48  | 255.255.255.248 (/29) | 192.238.19.55  | 192.238.19.49 - 192.238.19.54 |
| A7     | 192.238.19.56  | 255.255.255.248 (/29) | 192.238.19.63  | 192.238.19.57 - 192.238.19.62 |
| A10    | 192.238.19.64  | 255.255.255.248 (/29) | 192.238.19.71  | 192.238.19.65 - 192.238.19.70 |
| A1     | 192.238.19.72  | 255.255.255.252 (/30) | 192.238.19.75  | 192.238.19.73 - 192.238.19.74 |
| A2     | 192.238.19.76  | 255.255.255.252 (/30) | 192.238.19.79  | 192.238.19.77 - 192.238.19.78 |
| A3     | 192.238.19.80  | 255.255.255.252 (/30) | 192.238.19.83  | 192.238.19.81 - 192.238.19.82 |
| A9     | 192.238.19.84  | 255.255.255.252 (/30) | 192.238.19.87  | 192.238.19.85 - 192.238.19.86 |
| A13    | 192.238.19.88  | 255.255.255.252 (/30) | 192.238.19.91  | 192.238.19.89 - 192.238.19.90 |
| A16    | 192.238.19.92  | 255.255.255.252 (/30) | 192.238.19.95  | 192.238.19.93 - 192.238.19.94 |
| A17    | 192.238.19.96  | 255.255.255.252 (/30) | 192.238.19.99  | 192.238.19.97 - 192.238.19.98 |
| A19    | 192.238.19.100 | 255.255.255.252 (/30) | 192.238.19.103 | 192.238.19.101 - 192.238.19.102 |
| A20    | 192.238.19.104 | 255.255.255.252 (/30) | 192.238.19.107 | 192.238.19.105 - 192.238.19.106 |

## Tree VLSM

![TREE VLSM1 drawio](https://github.com/user-attachments/assets/d334d7e0-a4b7-4749-9f36-a574a74401f2)

## Config Subnet




# GNS 3 CIDR
### Tree
![image](https://github.com/user-attachments/assets/e4c8442d-85c4-4f7d-9bf8-0ad9f4dc0864)

HoloLive
```
# DHCP config for eth0
auto eth0
iface eth0 inet dhcp
#	hostname ubuntu-1-1

# A3
auto eth1
iface eth1 inet static
	address 192.238.208.1
	netmask 255.255.255.252

# A1
auto eth2
iface eth2 inet static
	address 192.238.160.1
	netmask 255.255.255.252
#	gateway 192.168.2.1


# A2
auto eth3
iface eth3 inet static
	address 192.238.64.1
	netmask 255.255.255.252
#	gateway 192.168.3.1

```

Holo-EN
```
# A3
auto eth0
iface eth0 inet static
	address 192.238.208.2
	netmask 255.255.255.252
	gateway 192.238.208.1

# A17 
auto eth1
iface eth1 inet static
	address 192.238.196.1
	netmask 255.255.255.252
#	gateway 192.168.1.1


# A16
auto eth2
iface eth2 inet static
	address 192.238.200.33
	netmask 255.255.255.240
#	gateway 192.168.2.1

```
Holoadvent 

```
# A16
auto eth0
iface eth0 inet static
	address 192.238.200.34
	netmask 255.255.255.240
	gateway 192.238.200.33
#	up echo nameserver 192.168.0.1 > /etc/resolv.conf

# DHCP config for eth0
#auto eth0
#iface eth0 inet dhcp
#	hostname ubuntu-1-1

# A18
auto eth1
iface eth1 inet static
	address 192.238.200.1
	netmask 255.255.255.224
#	gateway 192.168.1.1
#	up echo nameserver 192.168.1.1 > /etc/resolv.conf
```

