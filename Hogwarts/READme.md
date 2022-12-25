# Hogwarts!
## @Author : M3tr1c_r00t

```
  ___ ___                                      __           ._.
 /   |   \  ____   ______  _  _______ ________/  |_  ______ | |
/    ~    \/  _ \ / ___\ \/ \/ /\__  \\_  __ \   __\/  ___/ | |
\    Y    (  <_> ) /_/  >     /  / __ \|  | \/|  |  \___ \   \|
 \___|_  / \____/\___  / \/\_/  (____  /__|   |__| /____  >  __
       \/       /_____/              \/                 \/   \/
       
```

### Enumeration...
_**Nmap...**_
```
# Nmap 7.92 scan initiated Fri Nov 18 22:24:31 2022 as: nmap -sC -sV -A -p 21,7441,7834,8740,9999,58048 -oN nmapports.txt 10.10.187.118
Nmap scan report for 10.10.187.118
Host is up (0.24s latency).

PORT      STATE  SERVICE VERSION
21/tcp    closed ftp
7441/tcp  open   ftp     vsftpd 3.0.3
|_ftp-anon: Anonymous FTP login allowed (FTP code 230)
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
|      At session startup, client count was 3
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
7834/tcp  open   http    PHP cli server 5.5 or later
|_http-title: Hogwart's Royal Entry
8740/tcp  open   ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.10 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 3a:50:82:7d:c1:94:17:f1:f1:fb:b9:ec:d3:81:2b:b5 (RSA)
|   256 49:62:ea:a2:16:2a:a1:f9:af:ea:9f:e3:d8:9a:a2:92 (ECDSA)
|_  256 22:c5:a5:22:ac:7c:df:8f:19:fe:15:89:7f:ee:90:49 (ED25519)
9999/tcp  open   abyss?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Fri, 18 Nov 2022 19:24:42 GMT
|     Content-Length: 0
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Fri, 18 Nov 2022 19:24:41 GMT
|_    Content-Length: 0
58048/tcp open   unknown
| fingerprint-strings: 
|   GenericLines: 
|     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
|     /||\x20 \n // // || \x20 \n // // || \x20 \n // \x20 || // \n // \x20 || // \x20
|     \x20|| // \n ===========||===========
|     -------------------------------------------------------~~
|     -Antioch, Cadmus and Ignotus Peverell
|     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
|     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
|     Death took a price, but I tell you for free, 
|     gifts that I had, I gave to these 3..
|_    last sighted in hogwa
2 services unrecognized despite returning data. If you know the service/version, please submit the following fingerprints at https://nmap.org/cgi-bin/submit.cgi?new-service :
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port9999-TCP:V=7.92%I=7%D=11/18%Time=63780627%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Fri,\x2018\x20Nov\x202
SF:022\x2019:24:41\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(HTTPOptions,
SF:4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Fri,\x2018\x20Nov\x202022\x2019:
SF:24:41\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(FourOhFourRequest,4B,"
SF:HTTP/1\.0\x20200\x20OK\r\nDate:\x20Fri,\x2018\x20Nov\x202022\x2019:24:4
SF:2\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(GenericLines,67,"HTTP/1\.1
SF:\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=ut
SF:f-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(RTSPReques
SF:t,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain
SF:;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request
SF:")%r(Help,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20te
SF:xt/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x2
SF:0Request")%r(SSLSessionReq,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nCo
SF:ntent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n
SF:\r\n400\x20Bad\x20Request")%r(TerminalServerCookie,67,"HTTP/1\.1\x20400
SF:\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\n
SF:Connection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(TLSSessionReq,67,
SF:"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20
SF:charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(
SF:Kerberos,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20tex
SF:t/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20
SF:Request")%r(LPDString,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent
SF:-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n4
SF:00\x20Bad\x20Request")%r(LDAPSearchReq,67,"HTTP/1\.1\x20400\x20Bad\x20R
SF:equest\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\
SF:x20close\r\n\r\n400\x20Bad\x20Request")%r(SIPOptions,67,"HTTP/1\.1\x204
SF:00\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r
SF:\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request");
==============NEXT SERVICE FINGERPRINT (SUBMIT INDIVIDUALLY)==============
SF-Port58048-TCP:V=7.92%I=7%D=11/18%Time=6378062B%P=x86_64-pc-linux-gnu%r(
SF:GenericLines,544,"\n~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
SF:~~~~~~\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\|\|\x20\x20\x20\x20\x20\x
SF:20\x20\x20\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20/\|\|\x20\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20/\x20\|\|\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20/\x20\x20\|\|\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20/\x20\x20\x20\|\|\x20\x20\x20\x20\x20\x20\x20\x20\x20\
SF:x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20/\x20\x2
SF:0\x20\x20\|\|\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x
SF:20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20//\x20\x20\x20/\|\|\\\x20\x20
SF:\x20\\\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20//\x20\x20//\x20\|\|\x20\\\x20\x20\\\n\x20\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20//\x20\x20/
SF:/\x20\x20\|\|\x20\x20\\\x20\x20\\\n\x20\x20\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20\x20//\x20\x20\\\x20\x20\x20\|\|\x20\x2
SF:0\x20//\x20\x20\\\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20
SF:\x20\x20\x20\x20//\x20\x20\x20\x20\\\x20\x20\|\|\x20\x20//\x20\x20\x20\
SF:x20\\\x20\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20
SF:\x20//\x20\x20\x20\x20\x20\x20\\\x20\|\|\x20//\x20\x20\x20\x20\x20\x20\
SF:\\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20====
SF:=======\|\|===========\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\|\|\x20\n
SF:-------------------------------------------------------~~\n\x20\x20\x20
SF:\x20\x20\x20\x20\x20\x20\x20\x20-Antioch,\x20Cadmus\x20and\x20Ignotus\x
SF:20Peverell\n~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\n
SF:~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\n\n\n\x20\x20
SF:\x20\x20Death\x20took\x20a\x20price,\x20but\x20I\x20tell\x20you\x20for\
SF:x20free,\x20\x20\x20\x20\x20\x20\n\x20\x20\x20\x20All\x20the\x20gifts\x
SF:20that\x20I\x20had,\x20I\x20gave\x20to\x20these\x203\.\.\n\x20\x20\x20\
SF:x20last\x20sighted\x20in\x20hogwa");
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.92%E=4%D=11/18%OT=7441%CT=21%CU=44632%PV=Y%DS=2%DC=T%G=Y%TM=637
OS:806EB%P=x86_64-pc-linux-gnu)SEQ(SP=102%GCD=1%ISR=10F%TI=Z%CI=I%II=I%TS=8
OS:)SEQ(SP=101%GCD=1%ISR=10E%TI=Z%II=I%TS=8)OPS(O1=M508ST11NW7%O2=M508ST11N
OS:W7%O3=M508NNT11NW7%O4=M508ST11NW7%O5=M508ST11NW7%O6=M508ST11)WIN(W1=68DF
OS:%W2=68DF%W3=68DF%W4=68DF%W5=68DF%W6=68DF)ECN(R=Y%DF=Y%T=40%W=6903%O=M508
OS:NNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R
OS:=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=
OS:AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=
OS:40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N%T=40%IPL=164%UN=0%RIPL=G%RID
OS:=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=40%CD=S)

Network Distance: 2 hops
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 21/tcp)
HOP RTT       ADDRESS
1   234.37 ms 10.8.0.1
2   234.46 ms 10.10.187.118

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Nov 18 22:27:55 2022 -- 1 IP address (1 host up) scanned in 203.93 seconds
```

Well, seeing that there's anonymous login , we can check it out...
There's a wierd directory named (...) after entering the directory there's another similar directory and after visiting it, we find a hidden zip file and a note....
![Screenshot_2022-12-14_15_30_24](https://user-images.githubusercontent.com/99975622/209465525-69269146-99b8-4156-b109-bd42f25cecd5.png)

After transfering the files to machine, note the zip file is encrypted. We can hash it using crackmapexec or john the ripper....

![Screenshot_2022-12-14_15_30_22](https://user-images.githubusercontent.com/99975622/209475309-712cfc86-b49a-4546-b977-a47d6d33a98a.png)
After unzipping the file, we get login creds which we can use in ssh...
![Screenshot_2022-12-14_15_30_43](https://user-images.githubusercontent.com/99975622/209475330-44311313-a7c4-4ac0-a80a-e0a5ca463aa0.png)
 We can now get the user flag....
 ### Priv Esc...

![Screenshot_2022-12-14_15_31_40](https://user-images.githubusercontent.com/99975622/209475338-2f40bcbe-ec74-4707-9759-b89026601449.png)
The box is vulnerable to pwnkit so we can use the python script to get root...

![Screenshot_2022-12-14_15_32_35](https://user-images.githubusercontent.com/99975622/209475366-49f060ae-7c9b-4a43-a60e-71992ec11930.png)
Done!
Now, Protect your Throne!! :)

## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/



