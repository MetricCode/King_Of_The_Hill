# King_Of_The_Hill
## @Author : M3tr1c_r00t
```

```
_**Nmap...**_
Being only 3 ports open, we dont have many options...
```
# Nmap 7.92 scan initiated Sun Nov 27 20:32:10 2022 as: nmap -sC -sV -A -v -oN nmapscan.txt 10.10.126.34
Nmap scan report for 10.10.126.34
Host is up (0.26s latency).
Not shown: 996 closed tcp ports (conn-refused)
PORT     STATE SERVICE VERSION
21/tcp   open  ftp     vsftpd 2.0.8 or later
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 ftp      ftp           400 Apr 29  2020 note
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:10.8.4.8
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 1
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 ff:ea:b0:58:35:79:df:b3:c1:57:01:43:09:be:2a:d5 (RSA)
|   256 3b:ff:4a:88:4f:dc:03:31:b6:9b:dd:ea:69:85:b0:af (ECDSA)
|_  256 fa:fd:4c:0a:03:b6:f7:1c:ee:f8:33:43:dc:b4:75:41 (ED25519)
80/tcp   open  http    Golang net/http server (Go-IPFS json-rpc or InfluxDB API)
|_http-title: Ellingson Mineral Company
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
9999/tcp open  abyss?
| fingerprint-strings: 
|   FourOhFourRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Sun, 27 Nov 2022 17:33:03 GMT
|     Content-Length: 11
|     Content-Type: text/plain; charset=utf-8
|     MetricCode
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest: 
|     HTTP/1.0 200 OK
|     Date: Sun, 27 Nov 2022 17:33:02 GMT
|     Content-Length: 11
|     Content-Type: text/plain; charset=utf-8
|_    MetricCode
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port9999-TCP:V=7.92%I=7%D=11/27%Time=6383C97E%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,80,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sun,\x2027\x20Nov\x202
SF:022\x2017:33:02\x20GMT\r\nContent-Length:\x2011\r\nContent-Type:\x20tex
SF:t/plain;\x20charset=utf-8\r\n\r\nMetricCode\n")%r(HTTPOptions,80,"HTTP/
SF:1\.0\x20200\x20OK\r\nDate:\x20Sun,\x2027\x20Nov\x202022\x2017:33:03\x20
SF:GMT\r\nContent-Length:\x2011\r\nContent-Type:\x20text/plain;\x20charset
SF:=utf-8\r\n\r\nMetricCode\n")%r(FourOhFourRequest,80,"HTTP/1\.0\x20200\x
SF:20OK\r\nDate:\x20Sun,\x2027\x20Nov\x202022\x2017:33:03\x20GMT\r\nConten
SF:t-Length:\x2011\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\n\r\
SF:nMetricCode\n")%r(GenericLines,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r
SF:\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close
SF:\r\n\r\n400\x20Bad\x20Request")%r(RTSPRequest,67,"HTTP/1\.1\x20400\x20B
SF:ad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConne
SF:ction:\x20close\r\n\r\n400\x20Bad\x20Request")%r(Help,67,"HTTP/1\.1\x20
SF:400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\
SF:r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(SSLSessionReq,
SF:67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\
SF:x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")
SF:%r(TerminalServerCookie,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nConte
SF:nt-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\
SF:n400\x20Bad\x20Request")%r(TLSSessionReq,67,"HTTP/1\.1\x20400\x20Bad\x2
SF:0Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection
SF::\x20close\r\n\r\n400\x20Bad\x20Request")%r(Kerberos,67,"HTTP/1\.1\x204
SF:00\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r
SF:\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(LPDString,67,"H
SF:TTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20ch
SF:arset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(LD
SF:APSearchReq,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20
SF:text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\
SF:x20Request")%r(SIPOptions,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nCon
SF:tent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\
SF:r\n400\x20Bad\x20Request");
Service Info: Host: Ellingson; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Nov 27 20:34:39 2022 -- 1 IP address (1 host up) scanned in 149.79 seconds
```
Luckily, we've got ftp open...
After logining in with ftp:ftp /anonymous:anonymous, we find a note...
![Screenshot_2022-11-27_20_33_40](https://user-images.githubusercontent.com/99975622/207656527-308477c4-f57e-4fe8-adf2-413337ab4f0c.png)
We can see that _**gcrawford**_ has been marked for weak passwords and exposing his crypo keys, for example, id_rsa key....

<br> On running a bruteforce, we can get his ftp password 
![Screenshot_2022-11-27_20_24_07](https://user-images.githubusercontent.com/99975622/207657452-ce70efa4-7ddd-467e-8718-cfd89fbd70e0.png)

Indeed we can find an rsa key file....
![Screenshot_2022-11-27_20_24_31](https://user-images.githubusercontent.com/99975622/207656195-08c684bc-761e-4bbb-a08f-22c3adc25463.png)
 But its encrypted.....
 <br> We can crack for the password using John-The-Ripper...
 
 ![Screenshot_2022-11-27_20_25_57](https://user-images.githubusercontent.com/99975622/207658031-9321f0fe-7416-4331-9c32-4237ef6cbdb7.png)

 And we get our passphrase...
 ![Screenshot_2022-11-27_20_27_49](https://user-images.githubusercontent.com/99975622/207658240-a868e7e7-86e6-4d85-b345-25ea0b47f8c9.png)
You can now ssh using the passphrase....
 
 ### Priv Esc ...
 The box is vulnerable to the  polkit CVE-2021-4034 vulnerability and we can use the python script to gain root access....

 ![Screenshot_2022-11-27_20_31_06](https://user-images.githubusercontent.com/99975622/207658953-24ac6bad-d182-4368-9f79-4686c523cf4e.png)

Its up to you now to protect your throne!
;)
## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/
 

