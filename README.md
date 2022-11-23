# pySysMon

---

### How to install the system monitor,

1. Go to your prefered folder location 

2. Open your CMD under that location

3. Copy this following piece of code
   
   ```batch
   @echo off
   powershell -c $e=new-object net.webclient ; $e.proxy=[net.webrequest]::getsystemwebproxy();$e.proxy.credentials=[net.credentialcache]::defaultcredentials;$e.downloadfile('https://github.com/maksudchowdhury/pySysMon/archive/refs/heads/main.zip','%cd%/pySysMon.zip')
   powershell Expand-Archive -LiteralPath pySysMon.zip -DestinationPath pySysMonExt
   del /f "pySysMon.zip"
   move %cd%\pySysMonExt\pySysMon-main %cd%
   rename "pySysMon-main" "pySysMon"
   rmdir "pySysMonExt"
   exit()
   ```

4. Paste the code in the terminal

5. Press enter

6. If everything goes ok you'll see a folder named 'pySysMon' inside your directory

7. Go to that folder

8. Open the CMD under 'pySysMon' folder location

9. To start the monitor type,
   
   ```bash
   python39 manage.py -s
   ```

10. To know more about the commands type,
    
    ```bash
    python39 manage.py -h
    ```
