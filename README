### Костылим сеть

```docker network create --opt encrypted --driver overlay --attachable web```

### Запускаем triefik
```docker compose -f traefik.yml up -d reverse-proxy```

### Запускаем наш домен
```docker compose -f whoami.yml up -d whoami```

### Проверяем
```curl -H Host:whoami.blabla.ru http://127.0.0.1```

### Инициируемся

```docker swarm init```

### Запускаем traefic

```docker stack deploy -c traefik.yml proxy```

### Размещаем наши сайты
```docker stack deploy -c whoami.yml whoami```

### Проверяем
```curl -H Host:whoami.blabla.ru http://127.0.0.1```
