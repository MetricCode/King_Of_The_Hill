# Lion!
## @Author : M3tr1c_r00t
```
          _____            _____                   _______                   _____          
         /\    \          /\    \                 /::\    \                 /\    \         
        /::\____\        /::\    \               /::::\    \               /::\____\        
       /:::/    /        \:::\    \             /::::::\    \             /::::|   |        
      /:::/    /          \:::\    \           /::::::::\    \           /:::::|   |        
     /:::/    /            \:::\    \         /:::/~~\:::\    \         /::::::|   |        
    /:::/    /              \:::\    \       /:::/    \:::\    \       /:::/|::|   |        
   /:::/    /               /::::\    \     /:::/    / \:::\    \     /:::/ |::|   |        
  /:::/    /       ____    /::::::\    \   /:::/____/   \:::\____\   /:::/  |::|   | _____  
 /:::/    /       /\   \  /:::/\:::\    \ |:::|    |     |:::|    | /:::/   |::|   |/\    \ 
/:::/____/       /::\   \/:::/  \:::\____\|:::|____|     |:::|    |/:: /    |::|   /::\____\
\:::\    \       \:::\  /:::/    \::/    / \:::\    \   /:::/    / \::/    /|::|  /:::/    /
 \:::\    \       \:::\/:::/    / \/____/   \:::\    \ /:::/    /   \/____/ |::| /:::/    / 
  \:::\    \       \::::::/    /             \:::\    /:::/    /            |::|/:::/    /  
   \:::\    \       \::::/____/               \:::\__/:::/    /             |::::::/    /   
    \:::\    \       \:::\    \                \::::::::/    /              |:::::/    /    
     \:::\    \       \:::\    \                \::::::/    /               |::::/    /     
      \:::\    \       \:::\    \                \::::/    /                /:::/    /      
       \:::\____\       \:::\____\                \::/____/                /:::/    /       
        \::/    /        \::/    /                 ~~                      \::/    /        
         \/____/          \/____/                                           \/____/         
                                                                                            
```
### Enumeration...
_**Nmap...**_
```
# Nmap 7.92 scan initiated Fri Dec 16 15:05:18 2022 as: nmap -sC -sV -A -v -oN nmapscan.txt 10.10.39.68
Nmap scan report for 10.10.39.68
Host is up (0.16s latency).
Not shown: 995 closed tcp ports (conn-refused)
PORT     STATE SERVICE VERSION
80/tcp   open  http    Apache httpd 2.4.18 ((Ubuntu))
|_http-title: Site doesn't have a title (text/html).
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
3306/tcp open  mysql   MySQL 5.7.19-0ubuntu0.16.04.1
| mysql-info: 
|   Protocol: 10
|   Version: 5.7.19-0ubuntu0.16.04.1
|   Thread ID: 6
|   Capabilities flags: 63487
|   Some Capabilities: ConnectWithDatabase, Speaks41ProtocolOld, DontAllowDatabaseTableColumn, ODBCClient, Support41Auth, SupportsTransactions, IgnoreSigpipes, FoundRows, InteractiveClient, Speaks41ProtocolNew, SupportsCompression, IgnoreSpaceBeforeParenthesis, LongPassword, SupportsLoadDataLocal, LongColumnFlag, SupportsMultipleStatments, SupportsMultipleResults, SupportsAuthPlugins
|   Status: Autocommit
|   Salt: KZ=~G\x1Fe\x1CY\x1F\x15b\x16g*%L-QB
|_  Auth Plugin Name: mysql_native_password
5555/tcp open  http    nginx 1.10.3 (Ubuntu)
|_http-title: Site doesn't have a title (text/html; charset=UTF-8).
| http-methods: 
|_  Supported Methods: GET HEAD POST
8080/tcp open  http    nostromo 1.9.6
|_http-title: Welcome
| http-methods: 
|_  Supported Methods: GET HEAD POST
9999/tcp open  abyss?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Fri, 16 Dec 2022 12:05:44 GMT
|     Content-Length: 0
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Fri, 16 Dec 2022 12:05:43 GMT
|_    Content-Length: 0
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port9999-TCP:V=7.92%I=7%D=12/16%Time=639C8946%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Fri,\x2016\x20Dec\x202
SF:022\x2012:05:43\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(HTTPOptions,
SF:4B,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Fri,\x2016\x20Dec\x202022\x2012:
SF:05:43\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(FourOhFourRequest,4B,"
SF:HTTP/1\.0\x20200\x20OK\r\nDate:\x20Fri,\x2016\x20Dec\x202022\x2012:05:4
SF:4\x20GMT\r\nContent-Length:\x200\r\n\r\n")%r(GenericLines,67,"HTTP/1\.1
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
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Dec 16 15:07:17 2022 -- 1 IP address (1 host up) scanned in 119.50 seconds
```

looking at port 8080, you can see that the server is nostromo which is outdated and vulnerable to an rce....

![Screenshot_2022-12-16_15_24_14](https://user-images.githubusercontent.com/99975622/209485406-d307205a-0082-4390-be02-7040ee9ca204.png)


Next, mirror the python exploit 

![Screenshot_2022-12-16_15_24_45](https://user-images.githubusercontent.com/99975622/209485447-43a38dea-30c9-4868-bccb-87c0a2461b73.png)

And we have code execution....

![Screenshot_2022-12-16_15_26_46](https://user-images.githubusercontent.com/99975622/209485463-7ab08c27-1d9f-433e-8a0f-84d513de4ccb.png)

Next, set up a reverse shell and we get a shell...
![Screenshot_2022-12-16_15_27_00](https://user-images.githubusercontent.com/99975622/209485496-ef68b8cf-478c-45a8-84d5-4d15105e467e.png)

### Priv Esc...
The system is vulnerable to CVE-2021-4034, so transfer the python script to the machine....
![Screenshot_2022-12-16_15_27_23](https://user-images.githubusercontent.com/99975622/209485563-751e25df-d719-43e6-b4ec-b7a9cfbc953a.png)

and we are root!


![Screenshot_2022-12-16_15_31_06](https://user-images.githubusercontent.com/99975622/209485570-b1583b63-bc7c-4783-8bee-50a29b53c92a.png)
Done!
<br> Now,Protect your King!
<br>:)


## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/







