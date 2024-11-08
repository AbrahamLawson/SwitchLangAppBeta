#  switchLang-frontend-app

# SwitchLangApp - Beta

SwitchLangApp est une application Web permettant de télécharger des vidéos et de les traduire à l'aide du speech-to-text. Actuellement en version Beta, cette application offre des fonctionnalités telles que l'upload de vidéos, la lecture dans un player intégré, et la gestion de la traduction dans plusieurs langues (comme l'anglais et le français).

---

## Fonctionnalités

- **Upload de vidéo** : Permet à l'utilisateur de télécharger des vidéos au format `.mp4` via un formulaire simple.
- **Lecture de vidéo** : Un player vidéo intégré permet de lire la vidéo téléchargée directement dans l'application.
- **Choix de la langue** : L'utilisateur peut choisir la langue pour la traduction (actuellement disponible : Anglais et Français).
- **API de traduction** : Envoi d'une requête à un backend pour traiter les traductions (fonction en développement).

---

## Installation

### Prérequis

Avant d'installer l'application, assurez-vous d'avoir les prérequis suivants installés sur votre machine :
- **Node.js** (version >=14)
- **npm** (version >=6)
- Un serveur backend pour l'API de traduction (fonctionnel en local : `http://localhost/api/projects-translations`)

### Cloner le projet

1. Clonez le repository avec Git :
   ```bash
   git clone https://github.com/votre-utilisateur/switchLangApp.git
   cd switchLangApp


## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```

