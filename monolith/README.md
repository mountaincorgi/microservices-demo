Build

```bash
docker build -t bul .
```

```bash
docker volume create bul-data
```

```bash
docker run -d \
    --name bul-app \
    --mount type=volume,src=bul-data,dst=/app/databases \
    -p 8000:8000 \
    bul
```

```bash
docker container ls -a
```
