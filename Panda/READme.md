# King_Of_The_Hill
## @Author : M3tr1c_r00t

```                                                                 
        ***** **                                 **               
     ******  ****                                 **              
    **   *  *  ***                                **              
   *    *  *    ***                               **              
       *  *      **                               **              
      ** **      **    ****    ***  ****      *** **      ****    
      ** **      **   * ***  *  **** **** *  *********   * ***  * 
    **** **      *   *   ****    **   ****  **   ****   *   ****  
   * *** **     *   **    **     **    **   **    **   **    **   
      ** *******    **    **     **    **   **    **   **    **   
      ** ******     **    **     **    **   **    **   **    **   
      ** **         **    **     **    **   **    **   **    **   
      ** **         **    **     **    **   **    **   **    **   
      ** **          ***** **    ***   ***   *****      ***** **  
 **   ** **           ***   **    ***   ***   ***        ***   ** 
***   *  *                                                        
 ***    *                                                         
  ******                                                          
    ***                                                           
                                                                  
```




_**Nmap**_
<br>
```
# Nmap 7.92 scan initiated Sun Nov 27 20:39:58 2022 as: nmap -sC -sV -A -p 22,53,80,139,445,1337,3306,5009,8080,9999 -oN nmapports.txt 10.10.102.118
Nmap scan report for 10.10.102.118
Host is up (0.22s latency).

PORT     STATE  SERVICE       VERSION
22/tcp   open   ssh           OpenSSH 7.4 (protocol 2.0)
| ssh-hostkey: 
|   2048 af:ff:dd:8f:74:ef:1b:ea:3a:33:7c:df:a0:e8:35:08 (RSA)
|   256 b5:dc:77:c4:15:a4:b6:5e:f3:07:46:ad:90:ea:d6:59 (ECDSA)
|_  256 a5:20:b4:a0:94:2a:27:f2:c9:ea:cb:09:f8:ab:f0:a6 (ED25519)
53/tcp   open   domain        ISC BIND 9.11.4-P2 (RedHat Enterprise Linux 7)
| dns-nsid: 
|_  bind.version: 9.11.4-P2-RedHat-9.11.4-9.P2.el7
80/tcp   open   http          Apache httpd 2.4.6 ((CentOS) PHP/5.6.40)
|_http-server-header: Apache/2.4.6 (CentOS) PHP/5.6.40
| http-methods: 
|_  Potentially risky methods: TRACE
|_http-title: Site doesn't have a title (text/html; charset=UTF-8).
139/tcp  open   netbios-ssn   Samba smbd 3.X - 4.X (workgroup: SAMBA)
445/tcp  open   netbios-ssn   Samba smbd 4.9.1 (workgroup: SAMBA)
1337/tcp open   http          nginx 1.16.1
|_http-server-header: nginx/1.16.1
|_http-title: Register Today
3306/tcp open   mysql         MariaDB (unauthorized)
5009/tcp closed airport-admin
8080/tcp open   http          Apache Tomcat/Coyote JSP engine 1.1
|_http-favicon: Apache Tomcat
|_http-server-header: Apache-Coyote/1.1
|_http-title: Apache Tomcat/7.0.92
9999/tcp open   abyss?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Sun, 27 Nov 2022 17:40:10 GMT
|     Content-Length: 0
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest: 
|     HTTP/1.0 200 OK
|     Date: Sun, 27 Nov 2022 17:40:06 GMT
|     Content-Length: 0
|   HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Sun, 27 Nov 2022 17:40:09 GMT
|_    Content-Length: 0
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port9999-TCP:V=7.92%I=7%D=11/27%Time=6383CB27%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sun,\x2027\x20Nov\x202
SF:022\x2017:40:06\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(HTTPOptions,
SF:4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sun,\x2027\x20Nov\x202022\x2017:
SF:40:09\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(FourOhFourRequest,4B,"
SF:HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sun,\x2027\x20Nov\x202022\x2017:40:1
SF:0\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(GenericLines,67,"HTTP/1\.1
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
Aggressive OS guesses: Linux 3.10 - 3.13 (95%), ASUS RT-N56U WAP (Linux 3.4) (94%), Linux 3.16 (94%), Linux 3.1 (93%), Linux 3.2 (93%), Linux 3.11 - 3.14 (92%), Linux 3.2 - 4.9 (92%), Linux 3.8 - 4.14 (92%), Ruckus ZoneFlex R710 WAP (Linux 3.4) (92%), AXIS 210A or 211 Network Camera (Linux 2.6.17) (92%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 2 hops
Service Info: Host: PANDA; OS: Linux; CPE: cpe:/o:redhat:enterprise_linux:7

Host script results:
| smb2-time: 
|   date: 2022-11-27T17:42:31
|_  start_date: N/A
|_clock-skew: mean: -1h19m57s, deviation: 2h53m12s, median: -2h59m57s
| smb2-security-mode: 
|   3.1.1: 
|_    Message signing enabled but not required
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.9.1)
|   Computer name: panda
|   NetBIOS computer name: PANDA\x00
|   Domain name: \x00
|   FQDN: panda
|_  System time: 2022-11-27T12:42:30-05:00
|_nbstat: NetBIOS name: PANDA, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| smb-security-mode: 
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)

TRACEROUTE (using port 5009/tcp)
HOP RTT       ADDRESS
1   151.50 ms 10.8.0.1
2   151.99 ms 10.10.102.118

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Nov 27 20:42:39 2022 -- 1 IP address (1 host up) scanned in 161.76 seconds

```
### Port 80
<br>

![Screenshot_2022-11-27_20_46_49](https://user-images.githubusercontent.com/99975622/207662162-c5ac0263-2001-4e7f-8f4c-7948f7034bbb.png)
If we Check the page source, we can find a username....

<br>
![Screenshot_2022-11-27_20_46_52](https://user-images.githubusercontent.com/99975622/207662345-4c0558f8-4ef3-4383-8919-4b2dca726577.png)
![Screenshot_2022-11-27_20_46_52](https://user-images.githubusercontent.com/99975622/207662345-4c0558f8-4ef3-4383-8919-4b2dca726577.png)
Well, i did a bruteforce on ssh using the username as a trend so as to save time and it worked lol.......

<br>
![Screenshot_2022-11-27_21_00_22](https://user-images.githubusercontent.com/99975622/207662598-3c173f32-b506-4df1-99c2-1b65f2dd7682.png)

### Priv Esc....
On checking our user permissions, we find that we can run the ftp binary as root...

![Screenshot_2022-11-27_21_03_23](https://user-images.githubusercontent.com/99975622/207662942-7becac7f-80f5-4171-8a80-052cdea5ecef.png)

We go to gtfobins and we find an exploit.....
<br>
![Screenshot_2022-11-27_21_09_50](https://user-images.githubusercontent.com/99975622/207662963-258bea72-2753-4890-9c7f-f3da2ec12b73.png)

And were root....
<br> If you fancy your throne, you wont lose it... 
<br> ;)

## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/



![Screenshot_2022-11-27_20_46_52](https://user-images.githubusercontent.com/99975622/207662345-4c0558f8-4ef3-4383-8919-4b2dca726577.png)
