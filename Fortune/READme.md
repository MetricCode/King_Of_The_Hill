# King_Of_The_Hill
## @ author : M3tr1c_r00t
## Fortune ....

```
 _______                                  
(_______)           _                     
 _____ ___   ____ _| |_ _   _ ____  _____ 
|  ___) _ \ / ___|_   _) | | |  _ \| ___ |
| |  | |_| | |     | |_| |_| | | | | ____|
|_|   \___/|_|      \__)____/|_| |_|_____)
                                          
```
### Enumeration...

```
# Nmap 7.93 scan initiated Sat Dec 24 14:47:45 2022 as: nmap -sC -sV -A -p 21,22,80,111,2049,3333,38291,40177,46249,54797 -oN nmapports.txt 10.10.243.204
Nmap scan report for 10.10.243.204
Host is up (0.15s latency).

PORT      STATE SERVICE    VERSION
21/tcp    open  ftp        vsftpd 3.0.3
22/tcp    open  ssh        OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 3eae1887b8c335b63aaf0ea4c3a2ef13 (RSA)
|   256 42cffe0dcb9224b98fdc11d410a7a03e (ECDSA)
|_  256 5cfcbcc93a01b1b678ac663c348f222a (ED25519)
80/tcp    open  http       Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Wheel of Fortune!
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
111/tcp   open  rpcbind    2-4 (RPC #100000)
| rpcinfo: 
|   program version    port/proto  service
|   100000  2,3,4        111/tcp   rpcbind
|   100000  2,3,4        111/udp   rpcbind
|   100000  3,4          111/tcp6  rpcbind
|   100000  3,4          111/udp6  rpcbind
|   100003  3           2049/udp   nfs
|   100003  3           2049/udp6  nfs
|   100003  3,4         2049/tcp   nfs
|   100003  3,4         2049/tcp6  nfs
|   100005  1,2,3      42541/udp   mountd
|   100005  1,2,3      53030/udp6  mountd
|   100005  1,2,3      54797/tcp   mountd
|   100005  1,2,3      60161/tcp6  mountd
|   100021  1,3,4      38209/udp   nlockmgr
|   100021  1,3,4      40177/tcp   nlockmgr
|   100021  1,3,4      42565/udp6  nlockmgr
|   100021  1,3,4      44967/tcp6  nlockmgr
|   100227  3           2049/tcp   nfs_acl
|   100227  3           2049/tcp6  nfs_acl
|   100227  3           2049/udp   nfs_acl
|_  100227  3           2049/udp6  nfs_acl
2049/tcp  open  nfs_acl    3 (RPC #100227)
3333/tcp  open  dec-notes?
| fingerprint-strings: 
|   GenericLines, GetRequest, HTTPOptions, JavaRMI, LPDString, NULL, kumo-server: 
|     UEsDBAoACQAAAHldmFX0UdhuHwAAABMAAAAJABwAY3JlZHMudHh0VVQJAAP15aZj9eWmY3V4CwAB
|     BAAAAAAEAAAAAKBMdEa1hgpcMccuP4svfYaam4TgHhOs9CtuGZu5z8NQSwcI9FHYbh8AAAATAAAA
|     UEsBAh4DCgAJAAAAeV2YVfRR2G4fAAAAEwAAAAkAGAAAAAAAAQAAAKSBAAAAAGNyZWRzLnR4dFVU
|_    BQAD9eWmY3V4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABAE8AAAByAAAAAAA=
38291/tcp open  mountd     1-3 (RPC #100005)
40177/tcp open  nlockmgr   1-4 (RPC #100021)
46249/tcp open  mountd     1-3 (RPC #100005)
54797/tcp open  mountd     1-3 (RPC #100005)
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port3333-TCP:V=7.93%I=7%D=12/24%Time=63A6E6E8%P=x86_64-pc-linux-gnu%r(N
SF:ULL,124,"UEsDBAoACQAAAHldmFX0UdhuHwAAABMAAAAJABwAY3JlZHMudHh0VVQJAAP15a
SF:Zj9eWmY3V4CwAB\nBAAAAAAEAAAAAKBMdEa1hgpcMccuP4svfYaam4TgHhOs9CtuGZu5z8N
SF:QSwcI9FHYbh8AAAATAAAA\nUEsBAh4DCgAJAAAAeV2YVfRR2G4fAAAAEwAAAAkAGAAAAAAA
SF:AQAAAKSBAAAAAGNyZWRzLnR4dFVU\nBQAD9eWmY3V4CwABBAAAAAAEAAAAAFBLBQYAAAAAA
SF:QABAE8AAAByAAAAAAA=\n")%r(GenericLines,124,"UEsDBAoACQAAAHldmFX0UdhuHwA
SF:AABMAAAAJABwAY3JlZHMudHh0VVQJAAP15aZj9eWmY3V4CwAB\nBAAAAAAEAAAAAKBMdEa1
SF:hgpcMccuP4svfYaam4TgHhOs9CtuGZu5z8NQSwcI9FHYbh8AAAATAAAA\nUEsBAh4DCgAJA
SF:AAAeV2YVfRR2G4fAAAAEwAAAAkAGAAAAAAAAQAAAKSBAAAAAGNyZWRzLnR4dFVU\nBQAD9e
SF:WmY3V4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABAE8AAAByAAAAAAA=\n")%r(LPDString,
SF:124,"UEsDBAoACQAAAHldmFX0UdhuHwAAABMAAAAJABwAY3JlZHMudHh0VVQJAAP15aZj9e
SF:WmY3V4CwAB\nBAAAAAAEAAAAAKBMdEa1hgpcMccuP4svfYaam4TgHhOs9CtuGZu5z8NQSwc
SF:I9FHYbh8AAAATAAAA\nUEsBAh4DCgAJAAAAeV2YVfRR2G4fAAAAEwAAAAkAGAAAAAAAAQAA
SF:AKSBAAAAAGNyZWRzLnR4dFVU\nBQAD9eWmY3V4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABA
SF:E8AAAByAAAAAAA=\n")%r(JavaRMI,124,"UEsDBAoACQAAAHldmFX0UdhuHwAAABMAAAAJ
SF:ABwAY3JlZHMudHh0VVQJAAP15aZj9eWmY3V4CwAB\nBAAAAAAEAAAAAKBMdEa1hgpcMccuP
SF:4svfYaam4TgHhOs9CtuGZu5z8NQSwcI9FHYbh8AAAATAAAA\nUEsBAh4DCgAJAAAAeV2YVf
SF:RR2G4fAAAAEwAAAAkAGAAAAAAAAQAAAKSBAAAAAGNyZWRzLnR4dFVU\nBQAD9eWmY3V4CwA
SF:BBAAAAAAEAAAAAFBLBQYAAAAAAQABAE8AAAByAAAAAAA=\n")%r(kumo-server,124,"UE
SF:sDBAoACQAAAHldmFX0UdhuHwAAABMAAAAJABwAY3JlZHMudHh0VVQJAAP15aZj9eWmY3V4C
SF:wAB\nBAAAAAAEAAAAAKBMdEa1hgpcMccuP4svfYaam4TgHhOs9CtuGZu5z8NQSwcI9FHYbh
SF:8AAAATAAAA\nUEsBAh4DCgAJAAAAeV2YVfRR2G4fAAAAEwAAAAkAGAAAAAAAAQAAAKSBAAA
SF:AAGNyZWRzLnR4dFVU\nBQAD9eWmY3V4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABAE8AAABy
SF:AAAAAAA=\n")%r(GetRequest,124,"UEsDBAoACQAAAHldmFX0UdhuHwAAABMAAAAJABwA
SF:Y3JlZHMudHh0VVQJAAP15aZj9eWmY3V4CwAB\nBAAAAAAEAAAAAKBMdEa1hgpcMccuP4svf
SF:Yaam4TgHhOs9CtuGZu5z8NQSwcI9FHYbh8AAAATAAAA\nUEsBAh4DCgAJAAAAeV2YVfRR2G
SF:4fAAAAEwAAAAkAGAAAAAAAAQAAAKSBAAAAAGNyZWRzLnR4dFVU\nBQAD9eWmY3V4CwABBAA
SF:AAAAEAAAAAFBLBQYAAAAAAQABAE8AAAByAAAAAAA=\n")%r(HTTPOptions,124,"UEsDBA
SF:oACQAAAHldmFX0UdhuHwAAABMAAAAJABwAY3JlZHMudHh0VVQJAAP15aZj9eWmY3V4CwAB\
SF:nBAAAAAAEAAAAAKBMdEa1hgpcMccuP4svfYaam4TgHhOs9CtuGZu5z8NQSwcI9FHYbh8AAA
SF:ATAAAA\nUEsBAh4DCgAJAAAAeV2YVfRR2G4fAAAAEwAAAAkAGAAAAAAAAQAAAKSBAAAAAGN
SF:yZWRzLnR4dFVU\nBQAD9eWmY3V4CwABBAAAAAAEAAAAAFBLBQYAAAAAAQABAE8AAAByAAAA
SF:AAA=\n");
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Aggressive OS guesses: Linux 3.1 (95%), Linux 3.2 (95%), AXIS 210A or 211 Network Camera (Linux 2.6.17) (94%), ASUS RT-N56U WAP (Linux 3.4) (93%), Linux 3.16 (93%), Adtran 424RG FTTH gateway (92%), Linux 2.6.32 (92%), Linux 2.6.39 - 3.2 (92%), Linux 3.1 - 3.2 (92%), Linux 3.2 - 4.9 (92%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 2 hops
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

TRACEROUTE (using port 111/tcp)
HOP RTT       ADDRESS
1   172.43 ms 10.8.0.1
2   172.57 ms 10.10.243.204

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Dec 24 14:48:12 2022 -- 1 IP address (1 host up) scanned in 31.25 seconds

```


### NB..
This box has many more ways to gain access than the one i'm gonna provide....
<br> Just be persistent ;) 

After the the usual scans, we find there's an open port, __**3333**__ 

<br> On visiting the page, we find there's some base64 code...

![Screenshot_2022-12-07_15_03_06](https://user-images.githubusercontent.com/99975622/206497811-64b3e05f-5bd8-468a-a4f3-410ab5d1abd6.png)
I run the usual base64 -d on my terminal but it brought some blob and i noticed a zip file header in it....
<br> So, its probably a file.....
<br> We can use a decoder on a site i.e from base64 to file... 
![Screenshot_2022-12-07_15_03_16](https://user-images.githubusercontent.com/99975622/206498236-455ab72d-561f-4ed4-88df-a17653cfd578.png)
And we get our zip file called application ....
<br>Downloaded it but when you try to unzip it, its asking for a password.
<br> We can do a bruteforce on the file to get its contents....
<br> In this scenario, i'm gonna use a John-The-Ripper and fcrackzip for demo purposes ....

![Screenshot_2022-12-07_15_06_34](https://user-images.githubusercontent.com/99975622/206499204-80e24bab-0a03-46f9-ac1e-da670f69be62.png)

__**fcrackzip ....**__
```
fcrackzip -v -u -D -p /usr/share/wordlists/rockyou.txt application.zip

```
**_John-The-Ripper..._**
```
zip2john application.zip > hash

john -w=/usr/share/wordlists/rockyou.txt hash

```
And we get the zip file password.....

![Screenshot_2022-12-07_15_06_55](https://user-images.githubusercontent.com/99975622/206500804-2cd0d1eb-4af4-4f08-a359-8a1ccb390430.png)
<br>
<br>After unziping our file... we get creds which we can use to login to ssh ....

![Screenshot_2022-12-07_15_07_37](https://user-images.githubusercontent.com/99975622/206501407-842c7a4c-d52f-4621-95cd-5faca6a6fde2.png)

#### Priv Esc....
Running sudo -l and we can see that the fortuna user can run the pico binary as root....

![Screenshot_2022-12-07_15_08_04](https://user-images.githubusercontent.com/99975622/206501747-087f1926-1ee9-49bb-a17b-8d2fea553cd1.png)

Immediately we can go to gtfobins and we can get to know how we can extract the binary....

After you run the binary using the given tags, we are taken to a kind of terminal.....
<br>In here, all of the commands you run will run as root....
<br> So we can set up a reverse shell and then run the reverses shell as root.....

![Screenshot_2022-12-07_15_10_24](https://user-images.githubusercontent.com/99975622/206502995-fbb97048-cc91-4ad8-8930-1ae7f5ba4c92.png)

And to run the command, use __**ctrl + T**__
<br>And boom! We have our connection ....
![Screenshot_2022-12-07_15_10_04](https://user-images.githubusercontent.com/99975622/206502204-17a521e6-f163-4fbd-8e4f-2ebb79574ff5.png)

#### All That Is Left Is To Protect your King Status! ;)

## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/
