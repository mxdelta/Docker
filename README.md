# Docker


если в /var/run/docker.sock есть то докер установлен

    обращение через API
echo -e "GET /containers/json HTTP/1.1\r\nHost: localhost\r\n\r\n" | nc local:/var/run/docker.sock

  установка контейнера

  apk add docker (для alpine-linux)

  просмотр процессов докера

  docker ps

  запуск нового контейнера

  docker run -v /:/mnt/(catpants) (alpine) ls -lha /mnt/(catpants)
  
