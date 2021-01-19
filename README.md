# 4)
 vercel -v : 21.1.0
# 5)
 vercel init // Puis sélectionner Angular
# 6) 
vercel // Puis Set up and deplay.... : Yes

=============

Linked to hug0br/tdvercel (created .vercel and added it to .gitignore)

�  Inspect: https://vercel.com/hug0br/tdvercel/upojg8u0n [2s]

✅  Production: https://tdvercel.vercel.app [copied to clipboard] [58s]

�  Deployed to production. Run `vercel --prod` to overwrite later (https://vercel.link/2F).

�  To change the domain or build command, go to https://vercel.com/hug0br/tdvercel/settings



# 7)
 vercel ls OU vercel list
# 8) 
vercel logs https://tdvercel.vercel.app/
# 9)
https://vercel.com/docs/cli#commands/inspect

Pour récupérer des informations sur un déploiement grâce a son url:

vercel inspect tdvercel-upojg8u0n.vercel.app

Exemple de retour : 

General

    id          dpl_ABod4qcbVA6aSpxu9sK8UEwWT5Sg
    name        tdvercel
    readyState  READY
    url         tdvercel-upojg8u0n.vercel.app


  Builds

    ┌ package.json        Ready               [47s]
    ├── favicon.ico
    ├── index.html
    ├── main-es2015.js
    ├── main-es2015.js.map
    ├── main-es5.js
    └── 17 output items hidden


  Routes

    ╶ ^/(.*)$             ->      /index.html
    ╶ ^/(?!.*api).*$      ->      /404.html      [404]
    ╶ error╶ filesystem

# 10)
Elles permettent d'injecter des valeurs que l'on ne souhaite pas mettre directement dans le code source, et donc de modifier le comportement du code en fonction de l'environnement dans lequel il s'exécute. 

Elles peuvent donc être modifiées selon l'environnement pour que l'application fonctionne d'une configuration à une autre. On peut donc développer une application et spécifier ce variables au moment de la mise en production : Exemple des informations de connexion à une base de données.

# 11) 
vercel env add plain mavar 

// Ensuite on lui donne une valeur et on sélectionne sa  portée (production/développement/preview)

# 12) 
Pour lister : vercel env ls


# 13)
vercel secrets est utilisée pour gérer les secrets utilisés dans les variables d'environnement sous un compte, en fournissant des fonctionnalités pour lister, ajouter, renommer et supprimer des secrets.

Peur remplir la valeur d'une variable d'environnement avec un secret. Ils sont cryptés et fournissent un moyen de stocker et de partager des informations sensibles entre les déploiements.

# 15)
On commence par créer un secret : 

vercel secrets add myclisecret mysecretvalueforcli

Puis on créer la variable d'environnement :

vercel env add secret mysecretvarcli

Puis dans la valeur du secret qui est demandée on fourni le secret créé au dessus : 

"myclisecret"

# 16) 
Il nous propose : production / preview / development

Cela permet d'avoir trois environnements distincts : La production, le développement et le test. Ainsi on peut développer sur l'application sans poser de soucis en cas de bugs sur l'appli en production.

L'environnement de prod est celui accessible par tous une fois l'application déployée.

Le test permet d'effectuer les tests avant la mise en production afin de faire remonter certains bugs qui peuvent être critiques en cas de mise en production immédiate

L'environnement de dev est l'environnement local utilisé par les développeurs pour mettre en place l'application.

# 18) 
DOMAINS

td-vercel-git-master.hug0br.vercel.app

td-vercel.hug0br.vercel.app

td-vercel-gamma.vercel.app

# 19)
https://github.com/Hug0Br/td_vercel/pull/1

Vercek déploie automatiquement la pull request : his pull request is being automatically deployed with Vercel

Le tout sur ce qui semble être un envirnnement de preview -> Test

Environnement Preview trigger pour que les tests soient effectués 

Screenshot dans les fichiers Git

# 20)
L'environnement de production est trigger lorsque la pull request a été accepté. Si la pull request a été accepté c'est qu'elle ne posera normalement pas de soucis et aura été testée au préalable dans l'environnement de test.

# 21)
L'environnement de production correspond a la branche master ou main selon ce qui a été choisis.

Les pull request permettent de tester du code dans l'environnemnt de preview afin d'observer le nouveau comportement de l'application une fois les modification effectuées. 

Si aucun bug n'est rencontré, on peut accepté la pull request et donc passer dans l'environnement de production.

Workflow : Création d'une branche pour la feature -> Développement de la nouvelle feature -> Push de la branche sur github -> Pull request -> test dans l'environnement preview -> Merge des branches dans l'environnement de production.

# 22)
Le serverless est un modèle dans lequel on fait appel a un service Cloud (comme Amazon AWS, Microsoft Azure ou Google Cloud Plateforme) afin d'héberger l'application. Ainsi les problèmes de maintenance matérielle, d'allocation de ressource, de gestion de la charge des serveurs, entre autres, ne sont plus de notre ressort.

Les développeurs fournissent le code et c'est le fournisseur qui gère tout le reste. LE développeur peut ainsi se concentrer uniquement sur le travail de développement, sans avoir la partie administration de serveur à gérer. 


