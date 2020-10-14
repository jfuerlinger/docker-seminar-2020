
# Allgemein

[Quelle - GitHub/rstropek](https://github.com/rstropek/DockerVS2015Intro/tree/master/dockerDemos/labs/040-dockerfile-node)

# Projekt initialisieren

## Projektverzeichnis initialisieren (package.json erzeugen)

```
docker run --rm -v /mnt/c/Projekte/HTL/Seminare/docker/labs/040-docker-node-express:/app -w /app node npm init -y
```

## Module installieren (express und handlbar)


```
docker run --rm -v /mnt/c/Projekte/HTL/Seminare/docker/labs/040-docker-node-express:/app -w /app node npm install express hbs

```

## Module installieren (types:express, copyfile und typescript)

```
docker run --rm -v /mnt/c/Projekte/HTL/Seminare/docker/labs/040-docker-node-express:/app -w /app node npm install -D @types/express copyfiles typescript
```

## Typescript initialisieren

```
docker run --rm -v /mnt/c/Projekte/HTL/Seminare/docker/labs/040-docker-node-express:/app -w /app node npx tsc --init
```



# Build Scripts adaptieren

```
{
  ...
  "scripts": {
    "build": "tsc && copyfiles --up 1 ./src/**/*.hbs ./dist",
    "start": "npm run build && node ./dist/app.js"
  },
  ...
}
```

# Build durchführen

```
docker run --rm -v /mnt/c/Projekte/HTL/Seminare/docker/labs/040-docker-node-express:/app -w /app node npm run build
 ```


# Web App starten

```
docker run --rm -v /mnt/c/Projekte/HTL/Seminare/docker/labs/040-docker-node-express:/app -w /app -p 7777:8080 node npm start
 ```

 [Web App öffnen](http://localhost:7777)

