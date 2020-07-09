---
title: Prise en main de MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server ou ReDim pour configurer une base de données sur un sous-système Windows pour Linux
description: Découvrez comment configurer MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server ou ReDim sur le sous-système Windows pour Linux.
keywords: WSL, Windows, windowssubsystem, MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server, Redims, Windows 10
ms.date: 07/07/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8ffd40ef21e8fb8ece529157852ba5d8bb676076
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2020
ms.locfileid: "86160220"
---
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a>Prise en main des bases de données sur le sous-système Windows pour Linux

Ce guide pas à pas vous aidera à vous familiariser avec la connexion de votre projet dans WSL à une base de données. Prise en main de MySQL, PostgreSQL, MongoDB, Redims, Microsoft SQL Server ou SQLite.

## <a name="prerequisites"></a>Prérequis

- Exécution de Windows 10, [mis à jour vers la version 2004](ms-settings:windowsupdate), **build 19041** ou ultérieure.
- [WSL activé et installé et mis à jour vers WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).
- [Distribution Linux installée](https://docs.microsoft.com/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (Ubuntu 18,04 pour nos exemples).
- Assurez-vous que votre distribution Ubuntu 18,04 s' [exécute en mode WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#set-your-distribution-version-to-wsl-1-or-wsl-2). (WSL peut exécuter des distributions en mode v1 ou v2.) Vous pouvez le vérifier en ouvrant PowerShell et en entrant :`wsl -l -v`

## <a name="differences-between-database-systems"></a>Différences entre les systèmes de base de données

Les choix les plus [populaires](https://insights.stackoverflow.com/survey/2019#technology-_-databases) pour un système de base de données sont les suivants :

- [MySQL](https://www.mysql.com/why-mysql/) (SQL)
- [PostgreSQL](https://www.postgresql.org/about/) (SQL)
- [Microsoft SQL Server](https://docs.microsoft.com/sql/?view=sql-server-ver15) (SQL)
- [SQLite](https://www.sqlite.org/about.html) (SQL)
- [MongoDB](https://www.mongodb.com/what-is-mongodb) (NoSQL)
- [ReDim](https://redis.io/topics/introduction) (NoSQL)

**MySQL** est une base de données relationnelle SQL Open source, qui organise les données dans une ou plusieurs tables dans lesquelles les types de données peuvent être liés entre eux. Il est évolutif verticalement, ce qui signifie qu’un ordinateur final fera le travail pour vous. Il est actuellement le plus couramment utilisé par les quatre systèmes de base de données.

**PostgreSQL** (parfois appelé Postgres) est également une base de données relationnelle SQL Open source, mettant l’accent sur l’extensibilité et la conformité aux normes. Il peut désormais gérer JSON, mais il est généralement recommandé pour les données structurées, la montée en charge verticale et les besoins ACID, tels que le commerce électronique et les transactions financières.

**Microsoft SQL Server** comprend SQL Server sur Windows, SQL Server sur Linux et SQL sur Azure. Il s’agit également de systèmes de gestion de base de données relationnelle configurés sur des serveurs avec fonction principale de stockage et de récupération des données, comme demandé par les applications logicielles.

**SQLite** est une base de données autonome, basée sur des fichiers et autonome,, connue pour la portabilité, la fiabilité et les bonnes performances, même dans les environnements à faible mémoire.

**MongoDB** est une base de données de documents NoSQL Open source conçue pour fonctionner avec JSON et stocker des données sans schéma. Il est évolutif horizontalement, ce qui signifie que plusieurs machines plus petites feront le travail pour vous. C’est parfait pour la flexibilité, les données non structurées et la mise en cache des analyses en temps réel.

**Redims** est un magasin de structures de données en mémoire NoSQL Open source. Il utilise des paires clé-valeur pour le stockage au lieu de documents. Les insertions sont connues pour sa flexibilité, ses performances et sa prise en charge de langages étendus. Elle est suffisamment flexible pour être utilisée comme un cache ou un courtier de messages et peut utiliser des structures de données telles que des listes, des jeux et des hachages.

Le tri de la base de données que vous choisissez doit dépendre du type d’application avec lequel vous allez utiliser la base de données. Nous vous recommandons de rechercher les avantages et les inconvénients des bases de données structurées et non structurées et de choisir en fonction de votre cas d’utilisation.

## <a name="install-mysql"></a>Installer MySQL

Pour installer MySQL sur WSL (Ubuntu 18,04) :

1. Ouvrez votre terminal WSL (par ex. Ubuntu 18.04).
2. Mettez à jour vos packages Ubuntu : `sudo apt update`
3. Une fois les packages mis à jour, installez MySQL avec :`sudo apt install mysql-server`
4. Confirmez l’installation et récupérez le numéro de version : `mysql --version`

Vous pouvez également exécuter le script de sécurité inclus. Cela modifie certaines des options par défaut les moins sécurisées pour des opérations telles que les connexions racine à distance et les exemples d’utilisateurs. Pour exécuter le script de sécurité :

1. Démarrer un serveur MySQL :`sudo /etc/init.d/mysql start`
2. Démarrez les invites de script de sécurité :`sudo mysql_secure_installation`
3. La première invite vous demande si vous souhaitez configurer le plug-in valider le mot de passe, qui peut être utilisé pour tester la force de votre mot de passe MySQL. Vous allez ensuite définir un mot de passe pour l’utilisateur racine MySQL, décider s’il faut ou non supprimer des utilisateurs anonymes, décider s’il faut autoriser l’utilisateur racine à se connecter à la fois localement et à distance, décider s’il faut supprimer la base de données de test et, enfin, décider s’il faut recharger immédiatement les tables de privilèges.

Pour ouvrir l’invite MySQL, entrez :`sudo mysql`

Pour afficher les bases de données disponibles, dans l’invite MySQL, entrez :`SHOW DATABASES;`

Pour créer une nouvelle base de données, entrez :`CREATE DATABASE database_name;`

Pour supprimer une base de données, entrez :` DROP DATABASE database_name;`

Pour plus d’informations sur l’utilisation des bases de données MySQL, consultez la [documentation MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/).

Pour travailler avec les bases de données MySQL dans VS Code, essayez l' [extension MySQL](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).

## <a name="install-postgresql"></a>Installation de PostgreSQL

Pour installer PostgreSQL sur WSL (Ubuntu 18,04) :

1. Ouvrez votre terminal WSL (par ex. Ubuntu 18.04).
2. Mettez à jour vos packages Ubuntu : `sudo apt update`
3. Une fois les packages mis à jour, installez PostgreSQL (et le package de contribution qui comporte des utilitaires utiles) avec : `sudo apt install postgresql postgresql-contrib`
4. Confirmez l’installation et récupérez le numéro de version : `psql --version`

3 commandes sont à connaître une fois PostgreSQL installé :

- `sudo service postgresql status` pour vérifier l’état de votre base de données.
- `sudo service postgresql start` pour commencer à exécuter votre base de données.
- `sudo service postgresql stop` pour arrêter l’exécution de votre base de données.

L’utilisateur administrateur par défaut, `postgres`, a besoin d’un mot de passe attribué afin de se connecter à une base de données. Pour définir un mot de passe :

1. Entrez la commande : `sudo passwd postgres`
2. Vous êtes invité à entrer votre nouveau mot de passe.
3. Fermez et ouvrez de nouveau votre terminal.

Pour exécuter PostgreSQL avec l’interpréteur de commandes [psql](https://www.postgresql.org/docs/10/app-psql.html) :

1. Démarrez votre service Postgres : `sudo service postgresql start`
2. Connectez-vous au service postgres et ouvrez le shell psql : `sudo -u postgres psql`

Une fois que vous avez correctement entré le shell psql, la modification de la ligne de commande se présente comme suit : `postgres=#`

> [!NOTE]
> Vous pouvez également ouvrir le shell psql en basculant vers l’utilisateur postgres avec : `su - postgres` puis en entrant la commande : `psql`.

Pour quitter postgres = # Enter : `\q` ou utilisez la touche de raccourci : Ctrl + D

Pour connaître les comptes d’utilisateur qui ont été créés sur votre installation PostgreSQL, utilisez : `psql -c "\du"` à partir de votre terminal WSL... ou simplement `\du` si le shell psql est ouvert. Cette commande affiche les colonnes : nom d’utilisateur du compte, liste des attributs des rôles et membre du ou des groupes de rôles. Pour quitter et revenir à la ligne de commande, entrez : `q`.

Pour plus d’informations sur l’utilisation des bases de données PostgreSQL, consultez les [documents PostgreSQL](https://www.postgresql.org/docs/13/tutorial-createdb.html).

Pour travailler avec les bases de données PostgreSQL dans VS Code, essayez l' [extension PostgreSQL](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).

## <a name="install-mongodb"></a>Installation de MongoDB

Pour installer MongoDB sur WSL (Ubuntu 18,04) :

1. Ouvrez votre terminal WSL (par ex. Ubuntu 18.04).
2. Mettez à jour vos packages Ubuntu : `sudo apt update`
3. Une fois les packages mis à jour, installez MongoDB avec : `sudo apt-get install mongodb`
4. Confirmez l’installation et récupérez le numéro de version : `mongod --version`

3 commandes sont à connaître une fois MongoDB installée :

- `sudo service mongodb status` pour vérifier l’état de votre base de données.
- `sudo service mongodb start` pour commencer à exécuter votre base de données.
- `sudo service mongodb stop` pour arrêter l’exécution de votre base de données.

> [!NOTE]
> Vous pouvez voir la commande `sudo systemctl status mongodb` utilisée dans des tutoriels ou des articles. Afin d’alléger le système, WSL n’inclut pas `systemd` (système de gestion de service dans Linux). Au lieu de cela, il utilise SysVinit pour démarrer les services sur votre ordinateur. Vous ne devriez pas remarquer de différence. Toutefois, si un tutoriel recommande l’utilisation de `sudo systemctl`, utilisez plutôt `sudo /etc/init.d/`. Par exemple, `sudo systemctl status mongodb`, pour WSL ce serait `sudo /etc/inid.d/mongodb status`. Vous pouvez également utiliser `sudo service mongodb status`.

Pour exécuter votre base de données Mongo sur un serveur local :

1. Vérifiez l’état de votre base de données : `sudo service mongodb status` vous devez voir une réponse [Fail], sauf si vous avez déjà démarré votre base de données.

2. Démarrez votre base de données : `sudo service mongodb start` vous devez maintenant voir une réponse [OK].

3. Vérifiez en vous connectant au serveur de base de données et en exécutant une commande de diagnostic : `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` cela produira la version actuelle de la base de données, l’adresse et le port du serveur, ainsi que la sortie de la commande status. La valeur `1` du champ « OK » dans la réponse indique que le serveur fonctionne.

4. Pour arrêter l’exécution du service MongoDB, entrez : `sudo service mongodb stop`

> [!NOTE]
> MongoDB possède plusieurs paramètres par défaut, notamment le stockage des données dans/Data/DB et leur exécution sur le port 27017. En outre, `mongod` est le démon (processus hôte pour la base de données) et `mongo` est le shell de ligne de commande qui se connecte à une instance spécifique de `mongod`.

VS Code prend en charge l’utilisation des bases de données MongoDB à l’aide de l' [extension Azure CosmosDB](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb), vous pouvez créer, gérer et interroger des bases de données MongoDB à partir d’vs code. Pour plus d’informations, consultez la VS Code documentation : [utilisation de MongoDB](https://code.visualstudio.com/docs/azure/mongodb).

Pour en savoir plus, consultez la documentation MongoDB :

- [Présentation de l’utilisation de MongoDB](https://docs.mongodb.com/manual/introduction/)
- [Créer des utilisateurs](https://docs.mongodb.com/manual/tutorial/create-users/)
- [Se connecter à une instance MongoDB sur un hôte distant](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [CRUD : créer, lire, mettre à jour, supprimer](https://docs.mongodb.com/manual/crud/)
- [Documentation de référence](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a>Installer Microsoft SQL Server

Pour installer SQL Server sur WSL (Ubuntu 18,04), suivez ce guide de démarrage rapide : [installer SQL Server et créer une base de données sur Ubuntu](https://docs.microsoft.com/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15).

Pour utiliser Microsoft SQL Server bases de données dans VS Code, essayez l' [extension MSSQL](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).

## <a name="install-sqlite"></a>Installer SQLite

Pour installer SQLite sur WSL (Ubuntu 18,04) :

1. Ouvrez votre terminal WSL (par ex. Ubuntu 18.04).
2. Mettez à jour vos packages Ubuntu : `sudo apt update`
3. Une fois les packages mis à jour, installez SQLite3 avec :`sudo apt install sqlite3`
4. Confirmez l’installation et récupérez le numéro de version : `sqlite3 --version`

Pour créer une base de données de test, appelée « example. DB », entrez :`sqlite3 example.db`

Pour afficher la liste de vos bases de données SQLite, entrez :`.databases`

Pour afficher l’état de votre base de données, entrez :`.dbinfo ?DB?`

Pour quitter l’invite SQLite, entrez :`.exit`

Pour plus d’informations sur l’utilisation d’une base de données SQLite, consultez la [documentation SQLite](https://www.sqlite.org/quickstart.html).

Pour travailler avec les bases de données SQLite dans VS Code, essayez l' [extension SQLite](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).

## <a name="install-redis"></a>Installer les ReDim

Pour installer les éléments ReDim sur WSL (Ubuntu 18,04) :

1. Ouvrez votre terminal WSL (par ex. Ubuntu 18.04).
2. Mettez à jour vos packages Ubuntu : `sudo apt update`
3. Une fois les packages mis à jour, installez les éléments ReDim avec :`sudo apt install redis-server`
4. Confirmez l’installation et récupérez le numéro de version : `redis-server --version`

Pour commencer à exécuter votre serveur ReDim :`sudo service redis-server start`

Vérifiez si redims fonctionne (redims-CLI est l’utilitaire d’interface de ligne de commande pour communiquer avec les éléments ReDim) : `redis-cli ping` cela doit retourner une réponse de « pong ».

Pour arrêter l’exécution de votre serveur ReDim :`sudo service redis-server stop`

Pour plus d’informations sur l’utilisation d’une base de données Redims, consultez les [documents ReDim](https://redis.io/topics/quickstart).

Pour utiliser les bases de données Redims dans VS Code, essayez l' [extension redims](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).

## <a name="see-services-running-and-set-up-profile-aliases"></a>Voir services exécutant et configurer des alias de profil

Pour afficher les services en cours d’exécution sur votre distribution WSL, entrez :`service --status-all`

La saisie de `sudo service mongodb start` ou de `sudo service postgres start` et de `sudo -u postgrest psql` peut être fastidieuse.  Toutefois, vous pouvez envisager de configurer des alias dans votre fichier `.profile` sur WSL pour accélérer l’utilisation de ces commandes et vous en souvenir plus facilement.

Pour configurer votre propre alias personnalisé, ou raccourci, pour l’exécution de ces commandes :

1. Ouvrez votre terminal WSL et entrez `cd ~` pour vous assurer d’être dans le répertoire racine.
2. Ouvrez le fichier `.profile`, qui contrôle les paramètres de votre terminal, avec l’éditeur de texte de terminal, Nano : `sudo nano .profile`
3. En bas du fichier (ne modifiez pas les paramètres de `# set PATH`), ajoutez ce qui suit :

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    Cela permettra d’entrer `start-pg` pour commencer à exécuter le service postgresql et `run-pg` pour ouvrir le shell psql. Vous pouvez modifier `start-pg` et `run-pg` et choisir n’importe quel nom. Veillez simplement à ne pas remplacer une commande que postgres utilise déjà !

4. Une fois les nouveaux alias ajoutés, quittez l’éditeur de texte Nano à l’aide de la combinaison de touches **Ctrl + X**. Sélectionnez `Y` (Oui) lorsque vous êtes invité à enregistrer et à appuyer sur la touche Entrée (en laissant `.profile` comme nom de fichier).
5. Fermez et rouvrez votre terminal WSL, puis essayez vos nouvelles commandes d’alias.

## <a name="additional-resources"></a>Ressources supplémentaires

- [Configuration de votre environnement de développement sur Windows 10](https://docs.microsoft.com/windows/dev-environment/)
