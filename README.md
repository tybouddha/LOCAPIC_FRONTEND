LOCAPIC Frontend
Application mobile de géolocalisation développée avec React Native et Expo.
Prérequis
Avant de commencer, assurez-vous d'avoir installé :

Node.js (version 14 ou supérieure)
npm ou yarn
Expo CLI
Expo Go sur votre smartphone pour le développement

Installation

Clonez le dépôt :

bashCopygit clone https://github.com/tybouddha/LOCAPIC_FRONTEND.git
cd LOCAPIC_FRONTEND

Installez les dépendances :

bashCopynpm install
# ou
yarn install

Créez un fichier .env à la racine du projet :

envCopyAPI_BACKEND_URL=http://votre-backend-url:3000
Lancement de l'Application
Mode Développement
bashCopynpm start
# ou
yarn start
Cela lancera le serveur de développement Expo. Vous pourrez alors :

Scanner le QR code avec l'application Expo Go sur iOS/Android
Lancer l'application sur un émulateur
Ouvrir dans le navigateur web

Commandes Disponibles

npm start : Lance le serveur de développement
npm android : Lance l'application sur l'émulateur Android
npm ios : Lance l'application sur le simulateur iOS
npm web : Lance l'application en version web

Structure du Projet
CopyLOCAPIC_FRONTEND/
├── App.js
├── assets/
├── components/
│   ├── Map.js
│   └── PlacesList.js
├── screens/
│   ├── HomeScreen.js
│   ├── MapScreen.js
│   └── SignInScreen.js
├── reducers/
├── .env
├── app.json
└── package.json
Fonctionnalités
Authentification

Inscription utilisateur
Connexion utilisateur
Gestion de session avec tokens JWT

Carte et Localisation

Affichage de la carte interactive
Géolocalisation en temps réel
Ajout de marqueurs sur la carte
Sauvegarde des lieux favoris

Gestion des Places

Création de nouveaux lieux
Liste des lieux sauvegardés
Modification et suppression des lieux
Système de recherche

Configuration
Variables d'Environnement
Créez un fichier .env avec les variables suivantes :
envCopyAPI_BACKEND_URL=votre_url_backend
GOOGLE_MAPS_API_KEY=votre_clé_api_google_maps
Configuration Expo
Le fichier app.json contient la configuration principale de l'application :
jsonCopy{
  "expo": {
    "name": "LOCAPIC",
    "slug": "locapic",
    "version": "1.0.0",
    "orientation": "portrait",
    "icon": "./assets/icon.png",
    "splash": {
      "image": "./assets/splash.png",
      "resizeMode": "contain",
      "backgroundColor": "#ffffff"
    }
  }
}
Déploiement
Publication sur Expo

Créez un compte sur Expo
Connectez-vous via la CLI :

bashCopyexpo login

Publiez votre application :

bashCopyexpo publish
Génération des Builds
Pour Android :
bashCopyexpo build:android
Pour iOS :
bashCopyexpo build:ios
Tests
bashCopynpm test
# ou
yarn test
Dépendances Principales

@react-navigation/native : Navigation entre les écrans
@react-navigation/stack : Navigation stack
react-native-maps : Affichage des cartes
expo-location : Gestion de la géolocalisation
@reduxjs/toolkit : Gestion de l'état global
axios : Requêtes HTTP
react-native-paper : Composants UI

Bonnes Pratiques

Utilisez les composants réutilisables dans le dossier components/
Suivez la structure de navigation définie dans navigation/
Respectez les conventions de nommage React Native
Documentez les nouveaux composants et fonctionnalités

Contribution

Forkez le projet
Créez votre branche (git checkout -b feature/NouvelleFonctionnalite)
Committez vos changements (git commit -m 'Ajout de NouvelleFonctionnalite')
Poussez vers la branche (git push origin feature/NouvelleFonctionnalite)
Ouvrez une Pull Request

Support
Pour obtenir de l'aide :

Ouvrez une issue sur GitHub
Consultez la documentation d'Expo
Vérifiez les logs de développement

