# K0TH :) ; Fortuna ....
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


