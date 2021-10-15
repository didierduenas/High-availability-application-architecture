# Infrastructure immuable avec Docker
Dans cette démo, une image sera créée avec une application html utilisant ngnix comme serveur web.

## Installer Docker
- MacOs : https://docs.docker.com/docker-for-mac/install/
- Ubuntu et autres distributions linux : https://docs.docker.com/v17.12/install/linux/docker-ce/ubuntu/
- Windows : https://docs.docker.com/docker-for-windows/install/

## Créer un compte dans Docker hub
Docker hub est un Registry public où se trouvent plusieurs images de Docker avec différentes technologies installées. L’image utilisée dans cette démo est une image publique qui se trouve dans Docker hub. Vous devez créer un compte https://hub.docker.com/ pour publier l’image résultante.

## Authentifier votre Docker hube
```sh
# Entrer l’utilisateur et le mot de passe lorsque demandé
$ Docker login

````
## Construire l’image
```sh
$ cd Nginx-app
$ Docker build [DOCKERHUB_USER]/ngnix-app:v1
````
## Exécuter l’application
```sh
$ Docker run -it -p $host_port:80 [DOCKERHUB_USER]/ngnix-app:v1
````

## Publier l’image
```sh
$ Docker push [DOCKERHUB_USER]/ngnix-app:v1