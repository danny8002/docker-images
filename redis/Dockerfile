FROM mcr.microsoft.com/windows/servercore:ltsc2019

# download from https://www.memurai.com/
COPY bin/memurai-techpreview-v1.0.8-x64.msi C:/

RUN powershell.exe -Command Start-Process msiexec.exe -ArgumentList '/i', C:\\memurai-techpreview-v1.0.8-x64.msi, '/quiet', '/norestart' -NoNewWindow -Wait

CMD ["C:\\Program Files\\Memurai\\memurai.exe", "--protected-mode", "no"] 

EXPOSE 6379