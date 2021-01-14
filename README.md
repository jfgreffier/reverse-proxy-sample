# Exemple de reverse proxy

Mise en place d'un reverse proxy avec nginx en mode conteneurisé avec Docker.
Exemple avec trois services derrière le reverse proxy, conteneurisé eux aussi.

## Reference

[Article on Medium](https://medium.com/slickteam/configurer-votre-reverse-proxy-avec-nginx-et-docker-7c678c989080)

[Slickteam website](https://slickteam.fr)
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

## Author

Ronan Morel - [Website](https://ronanmorel.fr) | [Github](https://github.com/ronronan) | [Youtube](https://www.youtube.com/channel/UCu8f_ENFz0hPiwwCocJg2UA) | [Twitter](https://twitter.com/ronronan21) | [Medium](https://medium.com/@ronronan21)