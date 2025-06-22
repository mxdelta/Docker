# Docker


если в /var/run/docker.sock есть то докер установлен

    обращение через API
echo -e "GET /containers/json HTTP/1.1\r\nHost: localhost\r\n\r\n" | nc local:/var/run/docker.sock

  # установка DOCKER

  sudo apt-get install docker.io

    apk add docker (для alpine-linux)

    sudo systemctl enable docker

    sudo systemctl start docker

    sudo docker version

# Чтобы Докер работал без судо

     sudo usermod -aG docker $USER

         
 # просмотр процессов докера

    сборка Docker образа

    docker build -f Dockerfile -t tf2131(название) .
  
  docker ps

  запуск нового контейнера

       docker run --name web1 -p 80:80 -d nginx
  
       docker run -v /:/mnt/(catpants) (alpine) ls -lha /mnt/(catpants)
    
        docker run --rm -d -p 8080:80 --name web2 -v ~/web2:/usr/share/nginx/html nginx

# удаление контейнера

        docker rm <имя_контейнера>
        docker rm -f <имя_контейнера>
#  Устанавливаем Kubernetes

Существует несколько реализаций Kubernetes. Мы воспользуемся minikube. Для начала установим kubectl — инструмент командной строки для работы с кластером Kubernetes.
Устанавливаем kubectl:
$ curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl.
 

$ sudo install kubectl /usr/local/bin/kubectl.
$ kubectl version.
$ rm kubectl.



Устанавливаем minikube:
$ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64.
$ sudo install minikube-linux-amd64 /usr/local/bin/minikube.
$ rm minikube-linux-amd64.



Проверяем работоспособность: $ minikube version.

Поздравляю! Мы успешно развернули свой кластер k8s и вступаем в контейнерный бизнес!
