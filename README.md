# pySysMon

---

### How to install the system monitor,

1. Go to your prefered folder location 

2. Open your CMD under that location

3. Copy this following piece of code
   
   ```batch
   @echo off
   color 0a
   powershell -c $e=new-object net.webclient ; $e.proxy=[net.webrequest]::getsystemwebproxy();$e.proxy.credentials=[net.credentialcache]::defaultcredentials;$e.downloadfile('https://github.com/maksudchowdhury/pySysMon/archive/refs/heads/main.zip','%cd%/pySysMon.zip')
   powershell Expand-Archive -LiteralPath pySysMon.zip -DestinationPath pySysMonExt
   del /f "pySysMon.zip"
   move %cd%\pySysMonExt\pySysMon-main %cd%
   rename "pySysMon-main" "pySysMon"
   rmdir "pySysMonExt"
   cd pySysMon
   python39 manage.py -s
   ```

4. Paste the code in the terminal

5. Press enter

6. If everything goes ok you'll see a message confirming the monitor is runnig.

7. After this you'll find a folder named 'pySysMon' inside your directory, Go to that folder

8. Open the CMD under 'pySysMon' folder location

9. To know more about the commands type,
   
   ```bash
   python39 manage.py -h
   ```

### Some Screenshots of the system,



-  Initializing a CMD under a preferred location,

![1.png](C:\Users\Maksud\Pictures\1.png)



- After pasting the installation code from the GitHub readme file,

![2.png](C:\Users\Maksud\Pictures\2.png)



- Download and extraction phase of pySysMon files,

![3.png](C:\Users\Maksud\Pictures\3.png)



- After the system has initialized the first time,

![4.png](C:\Users\Maksud\Pictures\4.png)



- ' Help ' window of pySysMon,

![5.png](C:\Users\Maksud\Pictures\5.png)

#### Keep Learning & take care of yourself  .... 😁😁😁
