Example docker-compose.yml :

    docker-compose mpd
    mpd:
      hostname: mpd
      container_name: mpd
      build: ./docker-mpd
      ports:
        - "6600:6600"
      volumes:
         - "/home/tux/.config/mpd/:/etc/mpd/"
         - "/home/tux/mpd/:/var/lib/mpd/"
      devices:
        - /dev/snd
      restart: always
