# DEVOPS3
SET SAIL FOR THE AMAZING WORLD OF CONTAIN- ERS

Le but de ce projet est de conteneuriser et définir le déploiement d'une application web poll simple.
L'application est composée de 5 éléments :
- Poll, une application web Flask Python qui recueille les votes et les pousse dans une file d'attente Redis.
- Une file d'attente Redis, qui contient les votes envoyés par l'application Poll, en attendant qu'ils soient consommés par le Worker.
- Le Worker, une application Java qui consomme les votes se trouvant dans la file d'attente Redis, et les stocke dans une base de données PostgreSQL.
- Une base de données PostgreSQL, qui stocke (de manière persistante) les votes stockés par le Worker.
- Result, une application web Node.js qui récupère les votes de la base de données et affiche le résultat
