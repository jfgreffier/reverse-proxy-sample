# Exemple de reverse proxy

Mise en place d'un reverse proxy avec nginx en mode conteneurisé avec Docker.
Exemple avec trois services derrière le reverse proxy, conteneurisé eux aussi.

## Reference

[Article on Medium](https://medium.com/slickteam/configurer-votre-reverse-proxy-avec-nginx-et-docker-7c678c989080)

[Slickteam website](https://slickteam.fr)
## Informations techniques

### Lancer la démo

```bash
docker-compose up -d
```

### Mettre les DNS dans le fichier host

**Sous Windows**

Aller dans le dossier, via l'explorateur Windows, `C:\Windows\System32\drivers\etc` et modifier avec les droits administrateur le fichier `hosts`, avec ce contenu ci-dessous :

```
127.0.0.1 test.bzh
127.0.0.1 demo1.test.bzh
127.0.0.1 demo2.test.bzh
127.0.0.1 demo3.test.bzh
```

**Sous Linux**

Editer le fichier `/etc/hosts`, avec les droits administrateur, avec ce contenu ci-dessous :

```conf
127.0.0.1 test.bzh
127.0.0.1 demo1.test.bzh
127.0.0.1 demo2.test.bzh
127.0.0.1 demo3.test.bzh
```
### Tester les différents DNS :

* http://127.0.0.1 -> Page d'accueil
* http://test.bzh -> Page d'accueil

* http://test.bzh/demo1 -> Hello world  Nginx
* http://test.bzh/demo2 -> Httpd
* http://test.bzh/demo3 -> Hello world rancher

* http://demo1.test.bzh -> Hello world  Nginx
* http://demo2.test.bzh -> Httpd
* http://demo3.test.bzh -> Hello world rancher



## Author

Ronan Morel - [Website](https://ronanmorel.fr) | [Github](https://github.com/ronronan) | [Youtube](https://www.youtube.com/channel/UCu8f_ENFz0hPiwwCocJg2UA) | [Twitter](https://twitter.com/ronronan21) | [Medium](https://medium.com/@ronronan21)