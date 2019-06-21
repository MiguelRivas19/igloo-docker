# igloo-docker

Source: https://hub.docker.com/_/odoo

1. Démarrer la base de données PostgresSQL 9 pour les containeurs odoo 11:

docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres:9

2. Démarrer une instance Odoo 11:

docker run -v ~/eclipse-workspace/Igloo:/mnt/extra-addons -p 8069:8069 --name odoo --link db:db -t odoo:11

3. Redémarre un conteneur:
docker restart odoo

4. Supprimer un conteneur:
docker rm container odoo

# Instance installées

Instance de test
(cookbook):
docker run -v ~/eclipse-workspace/Igloo:/mnt/extra-addons -p 8069:8069 --name odoo-test --link db:db -t odoo:11

Gestion des changements
(Change Management):
docker run -v ~/eclipse-workspace/Igloo:/mnt/extra-addons -p 8061:8069 --name odoo-chm--link db:db -t odoo:11

Gestion des actifs du service et des éléments de configuration
(Service Actives and Configuration Item Management):
docker run -v ~/eclipse-workspace/Igloo:/mnt/extra-addons -p 8062:8069 --name odoo-sacm--link db:db -t odoo:11




