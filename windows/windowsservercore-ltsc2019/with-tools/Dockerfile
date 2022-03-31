FROM cdaecha/docker-jenkins:ltsc2019

# install chocolatey
RUN Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
RUN Invoke-Expression -Command "((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))"

# install 7z by choco
RUN choco install 7zip.install -y --ia "/D=C:\7z

# install git for windows by choco
RUN choco install git.install -y --params "/NoShellIntegration /NoGuiHereIntegration /NoOpenSSH /NoAutoCrlf" --ia "/D=C:\Git

# install .net framework sdk 4.8

# install .net core 2.1 sdk

# install .net core 3.1 sdk

# install node.js