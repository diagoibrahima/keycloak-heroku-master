# Deploy Keycloak to Heroku


Ce référentiel déploie la Keycloak (solution de gestion des identités et des accès) sur Heroku. Il est basé sur l'image de docker officielle de Keycloak avec quelques légères modifications pour utiliser les variables Heroku `PORT` et` DATABASE_URL` correctement.

Le déploiement se fera avec un dyno gratuit et une base de données Postgres gratuite attachée.

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

# Procédure
Pour le déploiement de ce service, nous avons utiliser l'image docker de keycloack. 

1. Création du repository github qui va accueillir les sources pour le déploiement du service.
2. En local sur notre machine on crée le fichier Dokerfile 
- Qui indique la version de l'image docker de keycloak utilisé
- Qui copie le script que l'image doit exécuter a son démarrage (docker-entrypoint.sh)
- Qui démarre le server jboss utilisé par keycloak 
3. Le fichier app.json contient les données de configuration du server a déployer sur heroku. Il est très utile si vous voulez déployer avec votre propre repo.
4. Apres la création des fichiers comme indiquer ci dessus, on fait un commit du projet vers github
>git init

>git remote add origin url_de_votre_repo

>git add .

>git commit

>git push -u origin master 

5. Après ces étapes cliquer sur le bouton de déploiement et remplissez les information nécessaire pour la création du dynos
6. Si vous rencontrez un problème de Permission denied alors faites pour que le script puisse avoir les autorisation nécessaire pour s’exécuter dans l'image docker

>git add --chmod=+x -- docker-entrypoint.sh

>git commit 

>git push origin master


**NB** : Sur heroku vous pouvez autoriser le déploiement automatique  qui permet de déployer a chaque fois que vous faites un push sur github.


contact me www.mmdiago.com for more explication
*for more informations*
