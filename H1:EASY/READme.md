# King_Of_The_Hill
## @Author : M3tr1c_r00t
```
 _   _ _ _____    _    ______   __
| | | / | ____|  / \  / ___\ \ / /
| |_| | |  _|   / _ \ \___ \\ V / 
|  _  | | |___ / ___ \ ___) || |  
|_| |_|_|_____/_/   \_\____/ |_|  

```

_**Nmap ...**_
```
# Nmap 7.92 scan initiated Mon Dec  5 18:52:22 2022 as: nmap -sC -sV -A -v -oN nmapscan.txt 10.10.221.177
Nmap scan report for 10.10.221.177
Host is up (0.17s latency).
Not shown: 994 closed tcp ports (conn-refused)
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 f7:75:95:c7:6d:f4:92:a0:0e:1e:60:b8:be:4d:92:b1 (RSA)
|   256 a2:11:fb:e8:c5:c6:f8:98:b3:f8:d3:e3:91:56:b2:34 (ECDSA)
|_  256 72:19:b7:04:4c:df:18:be:6b:0f:9d:da:d5:14:68:c5 (ED25519)
80/tcp   open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Apache2 Ubuntu Default Page: It works
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
8000/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)
| http-robots.txt: 1 disallowed entry 
|_/vbcms
|_http-title: VeryBasicCMS - Home
| http-methods: 
|_  Supported Methods: GET POST
8001/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
| http-title: My Website
|_Requested resource was /?page=home.php
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: Apache/2.4.29 (Ubuntu)
8002/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)
| http-methods: 
|_  Supported Methods: HEAD POST OPTIONS
|_http-title: Learn PHP
9999/tcp open  abyss?
| fingerprint-strings: 
|   FourOhFourRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Mon, 05 Dec 2022 15:52:50 GMT
|     Content-Length: 0
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest: 
|     HTTP/1.0 200 OK
|     Date: Mon, 05 Dec 2022 15:52:49 GMT
|_    Content-Length: 0
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port9999-TCP:V=7.92%I=7%D=12/5%Time=638E3E02%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Mon,\x2005\x20Dec\x2020
SF:22\x2015:52:49\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(HTTPOptions,4
SF:B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Mon,\x2005\x20Dec\x202022\x2015:5
SF:2:50\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(FourOhFourRequest,4B,"H
SF:TTP/1\.0\x20200\x20OK\r\nDate:\x20Mon,\x2005\x20Dec\x202022\x2015:52:50
SF:\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(GenericLines,67,"HTTP/1\.1\
SF:x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf
SF:-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(RTSPRequest
SF:,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;
SF:\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request"
SF:)%r(Help,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20tex
SF:t/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20
SF:Request")%r(SSLSessionReq,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nCon
SF:tent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\
SF:r\n400\x20Bad\x20Request")%r(TerminalServerCookie,67,"HTTP/1\.1\x20400\
SF:x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nC
SF:onnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(TLSSessionReq,67,"
SF:HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20c
SF:harset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(K
SF:erberos,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text
SF:/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20R
SF:equest")%r(LPDString,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-
SF:Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n40
SF:0\x20Bad\x20Request")%r(LDAPSearchReq,67,"HTTP/1\.1\x20400\x20Bad\x20Re
SF:quest\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x
SF:20close\r\n\r\n400\x20Bad\x20Request")%r(SIPOptions,67,"HTTP/1\.1\x2040
SF:0\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\
SF:nConnection:\x20close\r\n\r\n400\x20Bad\x20Request");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Dec  5 18:55:02 2022 -- 1 IP address (1 host up) scanned in 159.82 seconds

```
We can see there's a wierd port 8002 open....
![Screenshot_2022-12-05_18_53_01](https://user-images.githubusercontent.com/99975622/207177925-9e11cf8c-1ef7-42e5-843e-1c28b7dd48e5.png)

And on clicking try free lesson, we are given a pane to upload any php code....
![Screenshot_2022-12-05_18_53_12](https://user-images.githubusercontent.com/99975622/207178104-2d5d3637-fd94-418c-9a7b-6a82a4db5717.png)
You paste php reverse shell from github, change your ip and port then remove the php file extensions at the start and the endof the document...
<br>and we get access...
![Screenshot_2022-12-05_18_54_17](https://user-images.githubusercontent.com/99975622/207178469-faca48ff-9b57-43a6-9d76-6fb7546e7084.png)

_**Priv Esc...**_
<br>Navigate to the home directory of serv3 and we find a backup script being run as root after some period...
<br> We can make our own script to give us a reverse shell as root with the same name...
<br>Dont forget to make the file executable after uploading it to the system....
![Screenshot_2022-12-05_18_58_36](https://user-images.githubusercontent.com/99975622/207181123-eb909ddf-74fc-4aaa-a664-e670aa4274be.png)


