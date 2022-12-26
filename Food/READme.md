# Food!
## @Author : M3tr1c_r00t
```
 ______   ______     ______     _____    
/\  ___\ /\  __ \   /\  __ \   /\  __-.  
\ \  __\ \ \ \/\ \  \ \ \/\ \  \ \ \/\ \ 
 \ \_\    \ \_____\  \ \_____\  \ \____- 
  \/_/     \/_____/   \/_____/   \/____/ 
                                         
```

### Enumeration ...
_**Nmap...**_
```
# Nmap 7.92 scan initiated Mon Dec 26 03:22:59 2022 as: nmap -sC -sV -A -v -oN nmapscan.txt 10.10.146.49
Increasing send delay for 10.10.146.49 from 0 to 5 due to 55 out of 181 dropped probes since last increase.
Increasing send delay for 10.10.146.49 from 5 to 10 due to 11 out of 14 dropped probes since last increase.
Nmap scan report for 10.10.146.49
Host is up (0.15s latency).
Not shown: 996 closed tcp ports (conn-refused)
PORT     STATE    SERVICE     VERSION
22/tcp   open     ssh         OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 28:0c:0c:d9:5a:7d:be:e6:f4:3c:ed:10:51:49:4d:19 (RSA)
|   256 17:ce:03:3b:bb:20:78:09:ab:76:c0:6d:8d:c4:df:51 (ECDSA)
|_  256 07:8a:50:b5:5b:4a:a7:6c:c8:b3:a1:ca:77:b9:0d:07 (ED25519)
1839/tcp filtered netopia-vo1
3306/tcp open     mysql       MySQL 5.7.29-0ubuntu0.18.04.1
| mysql-info: 
|   Protocol: 10
|   Version: 5.7.29-0ubuntu0.18.04.1
|   Thread ID: 9
|   Capabilities flags: 65535
|   Some Capabilities: SupportsCompression, ODBCClient, IgnoreSpaceBeforeParenthesis, LongColumnFlag, ConnectWithDatabase, SupportsLoadDataLocal, IgnoreSigpipes, Speaks41ProtocolOld, SupportsTransactions, FoundRows, LongPassword, DontAllowDatabaseTableColumn, SwitchToSSLAfterHandshake, InteractiveClient, Speaks41ProtocolNew, Support41Auth, SupportsMultipleResults, SupportsMultipleStatments, SupportsAuthPlugins
|   Status: Autocommit
|   Salt: LY<8\x1B\x1FQR\x079AM\x7FT\x150w\x1E;
| 
|_  Auth Plugin Name: mysql_native_password
|_ssl-date: TLS randomness does not represent time
| ssl-cert: Subject: commonName=MySQL_Server_5.7.29_Auto_Generated_Server_Certificate
| Issuer: commonName=MySQL_Server_5.7.29_Auto_Generated_CA_Certificate
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2020-03-19T17:21:30
| Not valid after:  2030-03-17T17:21:30
| MD5:   a067 7d7d a831 9979 e1d7 4ca7 1e2f 5319
|_SHA-1: 5769 4d3d 4ff6 fce9 b4dd 1553 9799 9a97 0f1e 75e8
9999/tcp open     abyss?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Mon, 26 Dec 2022 00:23:54 GMT
|     Content-Length: 4
|     Content-Type: text/plain; charset=utf-8
|     king
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Mon, 26 Dec 2022 00:23:53 GMT
|     Content-Length: 4
|     Content-Type: text/plain; charset=utf-8
|_    king
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port9999-TCP:V=7.92%I=7%D=12/26%Time=63A8E999%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,78,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Mon,\x2026\x20Dec\x202
SF:022\x2000:23:53\x20GMT\r\nContent-Length:\x204\r\nContent-Type:\x20text
SF:/plain;\x20charset=utf-8\r\n\r\nking")%r(HTTPOptions,78,"HTTP/1\.0\x202
SF:00\x20OK\r\nDate:\x20Mon,\x2026\x20Dec\x202022\x2000:23:53\x20GMT\r\nCo
SF:ntent-Length:\x204\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\n
SF:\r\nking")%r(FourOhFourRequest,78,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20M
SF:on,\x2026\x20Dec\x202022\x2000:23:54\x20GMT\r\nContent-Length:\x204\r\n
SF:Content-Type:\x20text/plain;\x20charset=utf-8\r\n\r\nking")%r(GenericLi
SF:nes,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/pla
SF:in;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Reque
SF:st")%r(RTSPRequest,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Ty
SF:pe:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\
SF:x20Bad\x20Request")%r(Help,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nCo
SF:ntent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n
SF:\r\n400\x20Bad\x20Request")%r(SSLSessionReq,67,"HTTP/1\.1\x20400\x20Bad
SF:\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnect
SF:ion:\x20close\r\n\r\n400\x20Bad\x20Request")%r(TerminalServerCookie,67,
SF:"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20
SF:charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(
SF:TLSSessionReq,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x
SF:20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Ba
SF:d\x20Request")%r(Kerberos,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nCon
SF:tent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\
SF:r\n400\x20Bad\x20Request")%r(LPDString,67,"HTTP/1\.1\x20400\x20Bad\x20R
SF:equest\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\
SF:x20close\r\n\r\n400\x20Bad\x20Request")%r(LDAPSearchReq,67,"HTTP/1\.1\x
SF:20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-
SF:8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(SIPOptions,6
SF:7,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x
SF:20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Mon Dec 26 03:25:26 2022 -- 1 IP address (1 host up) scanned in 146.65 seconds

```
As there are not many possible options we can work with, we can try default creds on mysql and it works....

![Screenshot from 2022-12-26 03-25-54](https://user-images.githubusercontent.com/99975622/209486286-1245159c-d877-4a0d-9fdf-a6acbeb21abb.png)
We find some creds...
<br> We can try to ssh with them and we're in!

![Screenshot from 2022-12-26 03-26-44](https://user-images.githubusercontent.com/99975622/209486311-a36b861d-0392-4d20-81b3-bc6be44d1715.png)


### Priv Esc...
The System is vulnerable to the CVE-2021-4034 
<br> Transfer the python script to the server and boom! 
<br> We're root!

![Screenshot from 2022-12-26 03-27-51](https://user-images.githubusercontent.com/99975622/209486352-419d6ba4-b73a-47a8-8b3a-f034f8238c69.png)

Well, you know the drill!
<br> Defense is up to you!
<br> :)

## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/
