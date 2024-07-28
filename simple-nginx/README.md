## Simple Nginx with Docker

```shell
FROM nginx:1.10.1-alpine
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```

- docker build -t nginx .
- docker run -d –name nginx_app -p 8080:80 nginx
