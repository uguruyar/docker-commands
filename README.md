![Docker](https://user-images.githubusercontent.com/37346097/142766107-3221b265-7224-45ad-9dd2-8015c6f2ac48.png)

#### Docker 

Docker, uygulamalarınızı hızla derlemenize, test etmenize ve dağıtmanıza imkan tanıyan bir yazılım platformudur.

#### Image

Docker Image, Docker üzerinde çalışabilen bir container oluşturmak için bir dizi talimat içeren şablondur.

#### Container 

Docker Container’lar Docker Image'larının çalışan örnekleridir. Bir Image çalıştırmak bir Docker Container oluşturur.

![Docker](https://user-images.githubusercontent.com/37346097/142767309-0722ae13-685b-46e7-9327-1ce860a61d95.jpg)


# Docker-Commands

* ```docker images```
* ```docker image ls```

Docker Image'larını listeler.

* ```docker ps```

Çalışmakta olan containerları listeler.

* ```docker ps -a```

Çalışan çalışmayan bütün containerları listeler.

* ```docker ps -aq```

Docker üzerindeki bütün Container'ların ID'lerini listeler.






* ```docker pull <repository_name>/<image_name>:<image_tag>```

Belirtilen Image'ı local registry'e indirir.

* ```docker top <container_id>```

İlgili Container'da top komutunu çalıştırarak çıktısını gösterir.

* ```docker run -it <image_id|image_name> CMD```

Verilen Image'dan terminali attach ederek bir Container oluşturur.

* ```docker pause <container_id>```

İlgili Container'ı duraklatır.

* ```docker stop <container_id>```

İlgili Container'ı durdurur.

* ```docker start <container_id>```

İlgili Container'ı durdurulmuşsa tekrar başlatır.

* ```docker rm <container_id>```

İlgili Container'ı kaldırır fakat ilişkili Volume'lara dokunmaz.

* ```docker rm -v <container_id>```

İlgili Container'ı ilişkili Volume'lar ile birlikte kaldırır.

* ```docker rm -f <container_id>```

İlgili Container'ı zorlayarak kaldırır. Çalışan bir Container ancak -f ile kaldırılabilir.

* ```docker rmi <image_id|image_name>```

İlgili Image'u siler.

* ```docker rmi -f <image_id|image_name>```

İlgili Image'ı zorlayarak kaldırır. başka isimlerle Tag'lenmiş Image'lar -f ile kaldırılabilir.

* ```docker info```

Docker Daemon ile ilgili özet bilgiler verir.

* ```docker inspect <container_id>```

İlgili Container'la ilgili detaylı bilgiler verir.

* ```docker inspect <image_id|image_name>```

İlgili Image'la ilgili detaylı bilgiler verir.

* ```docker rm $(docker ps -aq)```

Dütün Container'ları kaldırır.

* ```docker stop $(docker ps -aq)```

Çalışan bütün Container'ları durdurur.

* ```docker rmi $(docker images -aq)```

Bütün Image'ları kaldırır.

* ```docker images -q -f dangling=true```

Dangling (Taglenmemiş ve bir Container ile ilişkilendirilmemiş) Image'ları listeler

* ```docker rmi $(docker images -q -f dangling=true)```

Dangling Image'ları listeler.

* ```docker volume ls -f dangling=true```

Dangling Volume'ları listeler.

* ```docker volume rm $(docker volume ls -f dangling=true -q)```

Dangling Volumeları kaldırır.

* ```docker logs <container_id>```

İlgili Container'ın terminalinde o ana kadar oluşan çıktıyı gösterir.

* ```docker logs -f <container_id>```

ilgili Container'ın terminalinde o ana kadar oluşan çıktıyı gösterir ve -f follow parametresi ile o andan sonra oluşan logları da göstermeye devam eder.
