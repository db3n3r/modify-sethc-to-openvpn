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

Linux
```bash
nmcli connection modify <nome-da-rede> connection.permissions ''
```

```vim
vim /etc/polkit-1/localauthority/50-local.d/10-vpn-login.pkla
```
```
[Enable VPN for Login Screen]
Identity=unix-user:*
Action=org.freedesktop.NetworkManager.settings.modify.system
ResultAny=yes
ResultInactive=yes
ResultActive=yes
```

```
sudo systemctl restart polkit
sudo systemctl restart NetworkManager
 ```


