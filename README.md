![Nginx](https://cdn.iconscout.com/icon/free/png-256/nginx-226030.png)

### Nginx + proxy reverso + load balancer

Exemplo utilizando docker.

Para rodar:
```sh
docker-compose up --detach
```

URL:
```curl
http://localhost:4747/
http://localhost:9999/
http://localhost:9998/
```

Proxy reverso apontando para server 9999 e 9998
```curl
http://localhost:4747/server1
http://localhost:4747/server2
```

Load balancer apontando para server 9999 e 9998. OBS: imagine esses dois servidores sendo a mesma aplicação
```curl
http://localhost:2222/
```