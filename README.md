# winrms

Script To Enable Winrm With SSL

**Kullanım:** 

- Admin yetkisi ile bir powershell açılır.
- `ConfigureRemotingForAnsible.ps1` scriptinin olduğu klasöre gidilir.
  ```
  cd C:\Users\Administrator\Downloads\
  ```
- Scriptin çalıştırılabilmesi aşağıdaki komutun çalıştırılması gerekmektedir. Sistem genelinde script çalıştırmaya izin vermez, yalnızca mevcut powershell'de script çalıştırmaya izin verir.
  ```
  C:\Users\Administrator\Downloads> Set-ExecutionPolicy Bypass -Scope Process 
  Execution Policy Change
  The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose
  you to the security risks described in the about_Execution_Policies help topic at
  http://go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy?
  [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
  ```
- Yalnızca belirli bir Ip Adresi için Winrm açılmak isteniyorsa
  ```
  .\ConfigureRemotingForAnsible.ps1 -Instance "IP_ADRESI" 
  ```
  Genel olarak Winrm açılmak isteniyorsa
  ```
  .\ConfigureRemotingForAnsible.ps1
  ```
