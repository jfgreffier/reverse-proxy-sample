# Exemple de reverse proxy

Mise en place d'un reverse proxy avec nginx en mode conteneurisé avec Docker.
Exemple avec trois services derrière le reverse proxy, conteneurisé eux aussi.

Pour plus d'information, vous pouvez retrouver mon article sur Medium : https://medium.com/slickteam/configurer-votre-reverse-proxy-avec-nginx-et-docker-7c678c989080


## Informations techniques

Lancer la démo :

```bash
docker-compose up -d
```

Et tester les différents DNS :
* http://127.0.0.1
* http://test.bzh
* http://demo1.test.bzh
* http://demo2.test.bzh
* http://demo3.test.bzh
