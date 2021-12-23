# Belajar Docker
Docker adalah ...

## Menginstal Docker 
```
https://docs.docker.com/engine/install/
```
Setelah selesai melakukan penginstalan, lanjut ke tahap menginstal image docker.

## Menginstall image docker
```
docker run --name <namanya> -p <portnya>:80 -d <nama_image>
```
- contoh
```
docker run --name website -p 8080:80 -d nginx
```

## Melihat container image yang sedang berjalan
```
docker ps
```

## Melihat container image yang sedang berjalan maupun yang tidak berjalan
```
docker ps -a
```
