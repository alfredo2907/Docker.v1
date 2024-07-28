## Create simple dockerfile with nginx and added new vhost with returning simple helloworld 

1. Add new vhost in `/etc/hosts/` (ex. edotest.local)
2. Create new directory with name content
3. Create new index.html inside of content directory
```shell
<html>
  <head>
    <title>LEARN Module 1!</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html>
```
4. Create dockerfile
```shell
FROM ubuntu:latest
RUN apt-get -y update && apt-get -y install nginx
COPY content/index.html /var/www/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```
5. Build the image
```shell
docker build -t nginx_with_vhost .
```
6. Running the image as a container 
```shell
docker run -d --name nginx_vhost -p 8081:80 nginx_with_vhost
```
## The Result

![Result](assets/result.png)
