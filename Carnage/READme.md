#  Carnage!
## @Author : M3tr1c_r00t
```
   ___                                     __ _                      _    
  / __|   __ _      _ _   _ _     __ _    / _` |   ___      o O O   | |   
 | (__   / _` |    | '_| | ' \   / _` |   \__, |  / -_)    o        |_|   
  \___|  \__,_|   _|_|_  |_||_|  \__,_|   |___/   \___|   TS__[O]  _(_)_  
_|"""""|_|"""""|_|"""""|_|"""""|_|"""""|_|"""""|_|"""""| {======|_| """ | 
"`-0-0-'"`-0-0-'"`-0-0-'"`-0-0-'"`-0-0-'"`-0-0-'"`-0-0-'./o--000'"`-0-0-' 
```

### Enumeraation...
Nmap ...
```
# Nmap 7.92 scan initiated Tue Dec  6 18:00:48 2022 as: nmap -sC -sV -A -v -oN nmapscan.txt 10.10.230.28
Increasing send delay for 10.10.230.28 from 0 to 5 due to 107 out of 355 dropped probes since last increase.
Nmap scan report for 10.10.230.28
Host is up (0.16s latency).
Not shown: 994 closed tcp ports (conn-refused)
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 6.7p1 Debian 5+deb8u8 (protocol 2.0)
| ssh-hostkey: 
|   1024 b1:ac:a9:92:d3:2a:69:91:68:b4:6a:ac:45:43:fb:ed (DSA)
|   2048 3a:3f:9f:59:29:c8:20:d7:3a:c5:04:aa:82:36:68:3f (RSA)
|   256 f9:2f:bb:e3:ab:95:ee:9e:78:7c:91:18:7d:95:84:ab (ECDSA)
|_  256 49:0e:6f:cb:ec:6c:a5:97:67:cc:3c:31:ad:94:a4:54 (ED25519)
80/tcp   open  http    Apache httpd 2.4.10 ((Debian))
|_http-server-header: Apache/2.4.10 (Debian)
|_http-title: Hill Studios - Index
|_http-favicon: Unknown favicon MD5: FED84E16B6CCFE88EE7FFAAE5DFEFD34
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
81/tcp   open  http    Apache httpd 2.4.10 ((Debian))
|_http-server-header: Apache/2.4.10 (Debian)
|_http-title: Hill Studios - Index
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
82/tcp   open  http    Apache httpd 2.4.10 ((Debian))
|_http-server-header: Apache/2.4.10 (Debian)
|_http-title: Hill Studios - Index
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
83/tcp   open  http    Apache httpd 2.4.10 ((Debian))
|_http-server-header: Apache/2.4.10 (Debian)
|_http-title: Site doesn't have a title (text/html).
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
9999/tcp open  abyss?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Tue, 06 Dec 2022 15:01:15 GMT
|     Content-Length: 0
|   GenericLines, Help, Kerberos, LDAPSearchReq, LPDString, RTSPRequest, SIPOptions, SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Tue, 06 Dec 2022 15:01:14 GMT
|_    Content-Length: 0
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Dec  6 18:02:50 2022 -- 1 IP address (1 host up) scanned in 122.08 seconds

```
Notice in port 82, we can upload a file, an image....
![Screenshot_2022-12-06_18_01_22](https://user-images.githubusercontent.com/99975622/210018860-623d6065-910b-41e9-8672-a66bc6d6d9d1.png)
So, head over to google and search for php reverse shell...
<br> Change the file type to gif then send the upload request to burpsuite....
![Screenshot_2022-12-06_18_03_10](https://user-images.githubusercontent.com/99975622/210019044-f0d1a4bb-abad-4b51-bb76-dcf531653f8c.png)
While on  burp suite,add the php file extension on the file then upload ....
<br> This is because there is some filtering going on which wont allow some file extensions and for this we can be able to exploit the double file extension upload...
```
https://prateek-gangwar.medium.com/validation-for-double-extension-file-upload-cc52ec688ff3
```
![Screenshot_2022-12-06_18_06_11](https://user-images.githubusercontent.com/99975622/210019147-ef4d5b6c-4207-40ea-8b08-20936c66f3af.png)
after changing the extension....

![Screenshot_2022-12-06_18_06_26](https://user-images.githubusercontent.com/99975622/210019450-2e0bc4bb-e813-44f4-b18e-7eae57cd412a.png)
Set up your listener, then curl the address to your file...

![Screenshot_2022-12-06_18_07_24](https://user-images.githubusercontent.com/99975622/210019529-4ca22aaa-da16-47e9-82fd-2776dffd9d7e.png)
And you get a shell...

### Priv Esc ...
Head over to the /tmp directory and you will find a tmux-0 file...
![Screenshot_2022-12-06_18_08_31](https://user-images.githubusercontent.com/99975622/210019875-0a612827-3603-47ac-975d-b204661366d5.png)
<br>There's a tmux vulnerability where you can hijack sessions that are run as root....
looking into the directory, you will find a session default owned by root....
```
https://book.hacktricks.xyz/linux-hardening/privilege-escalation#tmux-sessions-hijacking
```
For this, run the command
```
tmux -S attach default
```
and you will be root!
![Screenshot_2022-12-06_18_10_59](https://user-images.githubusercontent.com/99975622/210019941-01f42524-500f-43fc-96f9-e76c41fb8e47.png)




#### Note...

```
when you get to root, move out of the root directory, copy the koth binary and the flag into tmp directory then rename the folder to r00t or anything... 
Next create a new folder named root, copy the koth binary from tmp then flag and then echo your nickname to the king.txt
This is because of the 'e' file attribute.....
you can check files with this character by using ls -lZ *
you must have SELinux.....

```
The solution for now... :)
Now, protect your king!:)
## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/







