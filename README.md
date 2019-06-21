# igloo-docker

Source: https://hub.docker.com/_/odoo

1. Démarrer la base de données PostgresSQL 9 pour les containeurs odoo 11:

docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres:9

2. Démarrer une instance Odoo 11.

docker run -v ~/eclipse-workspace/Igloo:/mnt/extra-addons -p 8069:8069 --name odoo --link db:db -t odoo:11


