# Bài 2 - Nginx Web Server với Port Mapping

## 1. Khởi chạy container (chế độ ngầm -d, map cổng 8080:80)
```
04ab295eb866f2c342ac6cf2e47327883ad16117d3bcdfdf832bcb420db828c5
```

## 2. Kiểm tra container đang chạy
```
CONTAINER ID   IMAGE          COMMAND                  CREATED                  STATUS                  PORTS                                     NAMES
04ab295eb866   nginx:alpine   "/docker-entrypoint.…"   Less than a second ago   Up Less than a second   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   my-web
add23dbf9da7   my-vite-app    "/docker-entrypoint.…"   25 minutes ago           Up 25 minutes           0.0.0.0:3000->80/tcp, [::]:3000->80/tcp   vite-app
```

## 3. Gửi truy vấn curl http://localhost:8080
```
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, nginx is successfully installed and working.
Further configuration is required for the web server, reverse proxy, 
API gateway, load balancer, content cache, or other features.</p>

<p>For online documentation and support please refer to
<a href="https://nginx.org/">nginx.org</a>.<br/>
To engage with the community please visit
<a href="https://community.nginx.org/">community.nginx.org</a>.<br/>
For enterprise grade support, professional services, additional 
security features and capabilities please refer to
<a href="https://f5.com/nginx">f5.com/nginx</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```

## 4. Dọn dẹp (dừng và xóa container)
```
my-web
my-web
```
