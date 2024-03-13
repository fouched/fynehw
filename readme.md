# Setting up Dev environment
Open Powershell in admin mode

Run 

`Get-ExecutionPolicy` 

If it returns Restricted, run

`Set-ExecutionPolicy AllSigned`

Then run

`Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))`


Type 

`choco` 

to see if it worked

Install make

`choco install make`

Go to https://docs.fyne.io/started/ and choose the recommended MSYS2 for the C compiler


Note 
* Run the last step of the instructions to add compiler (MSYS2 MINGW64) to the path.

This makes working in GoLand / IntelliJ so MUCH easier

Below the export for my environment:
* `echo "export PATH=\$PATH:/c/dev/Go/bin:~/Go/bin" >> ~/.bashrc`


To get rid of terminal window for built executables:

`go build -ldflags -H=windowsgui`