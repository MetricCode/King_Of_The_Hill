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
remember to add
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

Now, protect your king!:)
## My socials:
<br>@ twitter: https://twitter.com/M3tr1c_root
<br>@ instagram: https://instagram.com/m3tr1c_r00t/

