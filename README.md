### Костылим сеть

```docker network create --opt encrypted --driver overlay --attachable web```

### Запускаем Traefik
```docker compose -f traefik.yml up -d reverse-proxy```

### Запускаем наш сайт
```docker compose -f whoami.yml up -d whoami```

### Проверяем
```curl -H Host:whoami.blabla.ru http://127.0.0.1```

### Инициируемся

```docker swarm init```

### Публикуем Traefik

```docker stack deploy -c traefik.yml proxy```

### Публикуем наш сайт
```docker stack deploy -c whoami.yml whoami```

### Проверяем
```curl -H Host:whoami.blabla.ru http://127.0.0.1```
