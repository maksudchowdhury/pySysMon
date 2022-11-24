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

![1](https://user-images.githubusercontent.com/45464612/203681612-7a979880-b474-4406-8fc8-b478b544f656.png)




- After pasting the installation code from the GitHub readme file,

![2](https://user-images.githubusercontent.com/45464612/203681635-2127bacf-4481-4f80-9959-461dfa3c038c.png)



- Download and extraction phase of pySysMon files,

![3](https://user-images.githubusercontent.com/45464612/203681661-37bc8cab-21c0-4aad-b1c9-43847568b4f0.png)




- After the system has initialized the first time,

![4](https://user-images.githubusercontent.com/45464612/203681683-1aad7b9c-4c06-407f-ae1d-29c07c2e101d.png)




- ' Help ' window of pySysMon,

![5](https://user-images.githubusercontent.com/45464612/203681705-2d17d094-2c6c-4fd1-bd3b-7339b20dff58.png)


#### Keep Learning & take care of yourself  .... 😁😁😁
