# Test Prisma

https://www.prisma.io/docs/getting-started/quickstart

Les migrations nécessitent une "Shadow database" qui est automatiquement créée puis supprimée à la volée par Prisma. Il faut donc que l'utilisateur connecté à la base de données ait la permission de créer des bases de données sur le serveur (d'où l'utilisation de l'utilisateur root ici, pour simplifier).

Lancement de la migration initiale (création d'un fichier de migration et mise à jour du modèle de données en fonction du fichier `prisma/schema.prisma`) :

```sh
npx prisma migrate dev --name init
```

La commande génère également le [Prisma Client](https://www.prisma.io/docs/concepts/components/prisma-client) dans `node_modules/@prisma/client` qui permet, en étant inclus dans notre code, d'interagir avec les objets enregistrés en base.
