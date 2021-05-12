Docker có 2 container cơ bản (có thể chuyển qua chuyển lại dễ dàng):
- Windown Container 
- Linux Container 

## Build và Run một image
```
> docker build -t getting-started<:v1> .
```

## Run

```
> docker run -dp 3000:3000 getting-started
```
```
> docker run -it --rm -p 8080:80 hello-aspnetcore<:v1>
```

*** Note: *** Để giữ kết nối khi thoát tra bấm tổ hợp phím Ctrl + Z,C


## Container

### Display ###
```
> docker container ls 
```

### To start an existing container which is stopped ###
```
> docker start <container-name/ID>
```

### To stop a running container ###
> docker stop <container-name/ID>
 
### Run Bash ##

```
> docker run -it -d [images-id] bin/bash
> docker exec -it CONTAINER_ID /bin/bash
```

## Share the application (Push/pull)

```
docker push docker/getting-started
```

```
docker login -u YOUR-USER-NAME
````


# Một số cầu lệnh khác:
- docker ps
- Sử dụng history để xem lịch sử những gì tạo trong image 
```
docker image history getting-started 
```

# Một số lỗi liên quan:

Containers feature is disabled. Enable it using the PowerShell script (in an administrative PowerShell) and restart your computer before using Docker Desktop: 
```
Enable-WindowsOptionalFeature -Online -FeatureName $("Microsoft-Hyper-V", "Containers") -All
```

##Fix Error context
```
> Command "images" not available in current context (22221aaa), you can use the "default" context to run this command
> docker context use default
```
