# Building and Running Image

Website the code is hosted on: https://ogow.dev

Reverse proxy config: https://www.youtube.com/watch?v=spbkCihFpQ8&ab_channel=BobbyIliev

```shell
$ docker build -t ogow.dev .
```

Serve the website on port 8081, live updates :D

```shell
$ docker run --mount type=bind,source=`pwd`/app,target=/usr/share/nginx/html --name ogow.dev -p 8081:80 -d ogow.dev
$ docker run -it -d --mount type=bind,source=`pwd`/app,target=/usr/share/nginx/html --name ogow.dev -p 8081:80 -d ogow.dev
```
