# Chapitre : DEPLOIEMENT (MERN)


## Héberger votre APP

L'hébergement d'une application e-commerce MERN complète (MongoDB, Express.js, React.js, Node.js) sur Microsoft Azure ou tout autre fournisseur de cloud implique plusieurs étapes. Vous trouverez ci-dessous un guide détaillé sur la manière de procéder : (ici, nous avons utilisé Microsoft Azure, mais vous pouvez choisir n'importe quel autre fournisseur)

1. **Configurer un compte Azure** :
   * Si vous n’en avez pas encore, créez un compte Microsoft Azure sur [https://azure.microsoft.com/](https://azure.microsoft.com/) .
   * Accédez au portail Azure ( [https://portal.azure.com/](https://portal.azure.com/) ) et connectez-vous avec les informations d’identification de votre compte.

![](https://i.imgur.com/8sqaQY9.png)

2. **Ressources de provision** :
   * Créez un nouveau groupe de ressources dans Azure pour organiser vos ressources de manière logique.
   * Au sein du groupe de ressources, provisionnez les ressources nécessaires :
     * **MongoDB** : vous pouvez choisir Azure Cosmos DB (un service de base de données multimodèle distribué à l’échelle mondiale) ou configurer une base de données MongoDB à l’aide de machines virtuelles Azure.
     * **App Service** : créez un plan App Service et une application Web pour héberger votre backend Node.js et votre frontend React.
     * **Stockage Azure** : vous pouvez également utiliser Stockage Azure pour stocker des ressources statiques telles que des images ou des fichiers.
3. **Configurer MongoDB** :
   * Si vous utilisez Azure Cosmos DB, suivez les instructions fournies dans le portail Azure pour créer un compte Cosmos DB et configurer une API MongoDB.
   * Si vous configurez MongoDB sur des machines virtuelles Azure, déployez une machine virtuelle, installez MongoDB et configurez-la pour autoriser les connexions à distance selon les besoins.
4. **Déployer le backend (Node.js)** :
   * Déployez votre backend Node.js sur Azure App Service.
   * Vous pouvez déployer à l’aide de Git, de GitHub Actions, d’Azure CLI ou directement depuis Visual Studio Code si vous utilisez l’extension Azure App Service.
   * Configurez les variables d’environnement dans le portail Azure ou à l’aide d’Azure CLI pour les chaînes de connexion à la base de données et d’autres configurations.
5. **Déployer le frontend (React.js)** :
   * Créez votre frontend React.js à l'aide **`npm run build`**de la commande.
   * Déployez les artefacts de build sur Azure App Service pour les applications Web statiques.
   * Comme pour le déploiement du backend, vous pouvez utiliser Git, GitHub Actions, Azure CLI ou Visual Studio Code pour le déploiement.
   * Configurez les variables d’environnement nécessaires pour le frontend, telles que les URL d’API du backend.
6. **Configurer le réseau** :
   * Configurez les règles de mise en réseau pour autoriser la communication entre votre backend et votre frontend.
   * Si vous utilisez Azure Cosmos DB, assurez-vous que votre backend peut se connecter à l’instance Cosmos DB en toute sécurité.

<iframe allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/INVodizZQCY"></iframe>
