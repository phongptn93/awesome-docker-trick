Docker có 2 container cơ bản (có thể chuyển qua chuyển lại dễ dàng):
- Windown Container 
- Linux Container 

# Một số cầu lệnh docker:
- docker ps
- docker container ls 
- docker 
docker run -d -p 80:80 docker/getting-started



Một số lỗi liên quan:
Containers feature is disabled. Enable it using the PowerShell script (in an administrative PowerShell) and restart your computer before using Docker Desktop: 

Enable-WindowsOptionalFeature -Online -FeatureName $("Microsoft-Hyper-V", "Containers") -All
