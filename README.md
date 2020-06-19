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


contact me www.mmdiago.com for more explication
