# Belajar Docker
Docker adalah platform yang dapat digunakan untuk memasukan dan menyatukan berbagai program, 
software maupun sistem operasi ke dalam suatu wadah yang disebut ***container***. 
Container tersebut nantinya akan memuat kumpulan ***image*** yang berisi data konfigurasi 
file serta pendukung lainnya.

## Docker installation

- https://docs.docker.com/engine/install/


## Pull Image
```
docker pull <image>
```
- contoh melakukan pull image dari https://hub.docker.com
```
docker pull nginx
```

## Melihat Image yang tersimpan
```
docker image ls
```
- atau
```
docker images
```

## Remove Image
- Catatan : Image dapat dihapus bila container telah dihentikan atau dihapus.
```
docker image rm <image_id>
```
- contoh
```
docker image rm 92511e4h66a3
```

## Running image
```
docker run --name <nama_containernya_bebas> -p <portnya_bebas>:80 -d <nama_image>
```
```
docker run -it <image_id> /bin/bash
```
- contoh
```
docker run --name website -p 8080:80 -d nginx
```
```
docker run -it 92511e4h66a3 /bin/bash
```

# Setelah dirunning maka Docker Image berubah menjadi Container
Perubahan ini di ikuti dengan adanya docker Container ID, yang berbeda dengan Image ID.

## Melihat container yang sedang berjalan
```
docker ps
```

## Melihat container yang sedang berjalan maupun yang tidak berjalan
```
docker ps -a
```

## Stop container
```
docker stop <container_id>
```
- contoh
```
docker stop 800000e4h66a3
```

## Start container
```
docker start <container_id>
```
- contoh
```
docker start 800000e4h66a3
```

## Debugging Cotainer melalui Interactive Terminal
```
docker exec -it <container_id> /bin/bash
```
- contoh
```
docker exec -it 800000e4h66a3 /bin/bash
```

## Melihat logs / riwayat aktivitas pada cotainer
```
docker logs <cotainer_id>
```
- contoh
```
docker logs 800000e4h66a3
```

## Remove container
```
docker rm -f <cotainer_id>
```
- contoh
```
docker rm -f 800000e4h66a3
```
