# CMS Web App - Active Audition Heyrieux

Cette application web permet de gérer les patients, les appels, les stocks d'appareils auditifs et les rendez-vous pour le centre Active Audition Heyrieux.

## Structure de l'application

L'application se compose des modules suivants :

- **index.html** : Page d'accueil avec navigation vers les différents modules
- **patients.html** : Gestion des patients et des rendez-vous ORL
- **calls.html** : Journal des appels reçus et passés
- **stock.html** : Gestion des stocks d'appareils auditifs
- **agenda.html** : Agenda de rappel pour les rendez-vous

## Configuration technique

Cette application utilise Firebase comme backend pour stocker et synchroniser les données. La configuration Firebase est déjà intégrée dans chaque fichier HTML.

## Mise en ligne de l'application

Pour partager cette application avec vos partenaires sans avoir besoin d'accéder au dossier racine, plusieurs solutions sont possibles :

### Option 1 : Déploiement sur Firebase Hosting (recommandé)

Cette option est recommandée car votre application utilise déjà Firebase pour les données. Cela permettra d'éviter les problèmes de CORS et de maintenir la cohérence de l'environnement.

1. Installez Node.js si ce n'est pas déjà fait : [https://nodejs.org/](https://nodejs.org/)

2. Installez Firebase CLI :
   ```
   npm install -g firebase-tools
   ```

3. Authentifiez-vous à Firebase :
   ```
   firebase login
   ```

4. Initialisez Firebase dans le dossier de l'application :
   ```
   cd /chemin/vers/CMS_Web_App
   firebase init
   ```
   - Sélectionnez "Hosting" quand on vous demande quelles fonctionnalités utiliser
   - Choisissez votre projet Firebase existant (celui qui contient déjà vos données)
   - Utilisez "." comme dossier public
   - Configurez comme une application à page unique : Non
   - Ne pas écraser les fichiers existants

5. Déployez l'application :
   ```
   firebase deploy
   ```

6. Une fois déployée, vous recevrez une URL (généralement https://votre-projet.web.app) que vous pourrez partager avec vos partenaires.

### Option 2 : Déploiement sur un service d'hébergement web standard

Si vous préférez utiliser un service d'hébergement web standard :

1. Souscrivez à un service d'hébergement web (ex: OVH, GoDaddy, etc.)
2. Téléchargez les fichiers de l'application sur le serveur via FTP ou le gestionnaire de fichiers du panneau de contrôle de l'hébergeur
3. Accédez à votre application via le domaine fourni par l'hébergeur

### Option 3 : Déploiement sur un service d'hébergement statique gratuit

Plusieurs services permettent d'héberger gratuitement des sites statiques :

#### GitHub Pages :

1. Créez un dépôt GitHub
2. Transférez tous les fichiers de l'application dans ce dépôt
3. Activez GitHub Pages dans les paramètres du dépôt
4. Votre site sera accessible à l'adresse https://[votre-nom-utilisateur].github.io/[nom-du-depot]

#### Netlify :

1. Créez un compte sur [Netlify](https://www.netlify.com/)
2. Glissez-déposez le dossier de l'application sur la page d'accueil de Netlify
3. Netlify génère automatiquement une URL pour votre site

## Remarques importantes

- Assurez-vous que les règles de sécurité de votre base de données Firebase sont correctement configurées pour protéger vos données
- Si vous utilisez un service d'hébergement autre que Firebase Hosting, vous devrez peut-être configurer CORS pour permettre l'accès à votre base de données Firebase

## Support et maintenance

Pour toute question ou problème, contactez TxAI Consult, le développeur de cette application.
