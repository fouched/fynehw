Open Powershell in admin mode

Run Get-ExecutionPolicy. If it returns Restricted, then run Set-ExecutionPolicy AllSigned

If it returns Restricted, then run Set-ExecutionPolicy AllSigned

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))


Type choco to see if it worked

choco install make


https://docs.fyne.io/started/

Follow the instructions

Note: do the last step to add compiler (MSYS2 MINGW64) to the path.
This makes working in GoLand / IntelliJ so MUCH easier

Below the export for my environment:
echo "export PATH=\$PATH:/c/dev/Go/bin:~/Go/bin" >> ~/.bashrc


To get rid of terminal window:
go build -ldflags -H=windowsgui