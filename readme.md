# Mesin Absensi / Fingerprint Solution X601 (ZKTeco)


- Model: Solution X601
- ZMM220-V1.2-140421 - nomor model modul
- Chip MultiBio 975 - ASIC/SoC fingerprint matching engine of ZKTeco
- Chip PME810816CBR - kemungkinan RAM (mirip part Winbond/ESMT yang di-rebrand)
- Realtek RTL8201CP - ini PHY Ethernet 10/100

Mainboard seri **ZKTeco iFace300/iFace302**, kemungkinan besar adalah rebrand/OEM dari ZKTeco iFace300 series (face + fingerprint access terminal), bukan desain custom dari nol.

Solution X601 is a high-capacity biometric time attendance and door access control terminal. It is built on ZKTeco's high-speed ZMM220 hardware platform (featuring a 1.2GHz processor) and uses firmware layouts often shared with the iFace300 multi-biometric architecture

## Related Devices
- ZKTeco ZMM220
- zkteco uface202
- https://www.zkteco.co.id/product/zkteco-uface202/
- https://zkteco.systems/en/product/uface202/

## Network

### Nmap Scan

```
Starting Nmap 7.95 ( https://nmap.org ) at 2026-11-07 22:53 WIB
Nmap scan report for 192.168.18.176
Host is up (0.00048s latency).
Not shown: 65531 closed tcp ports (reset)
PORT     STATE SERVICE
23/tcp   open  telnet
80/tcp   open  http
4360/tcp open  matrix_vnet
4370/tcp open  elpro_tunnel
MAC Address: 00:17:61:12:2F:80 (Private)

Nmap done: 1 IP address (1 host up) scanned in 2.56 seconds
```

### Telnet

```
nc 192.168.18.176 23
��������
Welcome to Linux (ZMM220) for MIPS
Kernel 3.0.8 on an MIPS
(none) login:


## Web

## Bug 1

- Upload file from http://192.168.18.176/form/Device?act=21
- then open http://192.168.18.176/csl/user?action=modify&uid=1
- the content is reflected

 http://192.168.18.176/form/ImportUser