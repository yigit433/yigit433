# Installation Github connection with SSH
In some operations we perform with Git, it may ask for a password, instead of entering the password each time, we install SSH.
We can make our job more practical.

## Installation steps
### Linux
```bash
ssh-keygen -t rsa -C "mailaddress"
eval `ssh-agent -s`
ssh-add <filepath>
cat <public key filepath>
```
### Windows
```powershell
ssh-keygen -t rsa -C "mailaddress"
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
ssh-add <filepath>
type <public key filepath>
```