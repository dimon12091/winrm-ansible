# Windows Host Setup
These scripts and configurations help setup the windows host to be managed by Ansible via WinRM.
You must have cert `..\ansible_server\client_cert.pem`.Step-by-step run scripts.

Before run scripts in PowerShell(run as Administrator) `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force`
```
.\enable_winrm.ps1 
```

```
.\import_client_cert.ps1 
```

```
.\create_ansible_user.ps1 
```

```
.\create_server_cert.ps1
```

```
.\create_winrm_listener.ps1 
```

```
.\update_firewall.ps1 
```