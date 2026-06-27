# SubTracker — Releases macOS

Dépôt public de **distribution** pour **SubTracker** : installateurs et mises à jour automatiques pour macOS.

> Ce dépôt ne contient **pas le code source**. Il héberge uniquement les binaires publiés via [GitHub Releases](https://github.com/mvsko/subtracker-releases/releases).

![macOS](https://img.shields.io/badge/plateforme-macOS-black?logo=apple)
![Dernière version](https://img.shields.io/github/v/release/mvsko/subtracker-releases?label=version)

---

## Sommaire

- [Qu'est-ce que SubTracker ?](#quest-ce-que-subtracker-)
- [Télécharger](#télécharger)
- [Installation](#installation)
- [Mises à jour automatiques](#mises-à-jour-automatiques)
- [Prérequis système](#prérequis-système)
- [Contenu d'une release](#contenu-dune-release)
- [Confidentialité](#confidentialité)
- [Signaler un problème](#signaler-un-problème)

---

## Qu'est-ce que SubTracker ?

**SubTracker** est une application macOS de suivi d'abonnements — locale, sans compte, sans serveur. Vos données restent sur votre Mac.

Fonctionnalités principales :

- Calendrier des prochains prélèvements et total mensuel
- Gestion des abonnements (ajout, édition, catalogue de services)
- Import CSV bancaire et export JSON / CSV
- Notifications locales avant facturation
- Interface en français ou anglais, thème clair / sombre

---

## Télécharger

| | |
|---|---|
| **Dernière version** | [Télécharger la dernière release](https://github.com/mvsko/subtracker-releases/releases/latest) |
| **Toutes les versions** | [Historique des releases](https://github.com/mvsko/subtracker-releases/releases) |

Pour une **première installation**, téléchargez le fichier `.dmg` correspondant à votre Mac :

| Architecture | Fichier |
|--------------|---------|
| Apple Silicon (M1, M2, M3…) | `SubTracker_X.X.X_aarch64.dmg` |

---

## Installation

1. Téléchargez le `.dmg` depuis la [dernière release](https://github.com/mvsko/subtracker-releases/releases/latest).
2. Ouvrez le fichier `.dmg`.
3. Glissez **SubTracker** dans le dossier **Applications**.
4. Lancez l'application depuis le Launchpad ou le Dock.

**Si macOS bloque l'ouverture** (application téléchargée depuis Internet) :

*Réglages Système → Confidentialité et sécurité → Ouvrir quand même*

---

## Mises à jour automatiques

À partir de la première version installée depuis ce dépôt, SubTracker peut se mettre à jour **depuis l'application** :

1. Ouvrez **Réglages**
2. Cliquez sur **Vérifier les mises à jour**
3. Si une version plus récente est disponible, installez-la en un clic — l'app redémarre automatiquement

Le mécanisme repose sur le [Tauri Updater](https://v2.tauri.app/plugin/updater/) : l'app consulte le manifeste `latest.json` publié ici, télécharge une archive signée (`.tar.gz`) et l'installe en local.

> La **première installation** se fait toujours manuellement via le `.dmg`. Les versions suivantes peuvent passer par le bouton de mise à jour dans l'app.

---

## Prérequis système

| | |
|---|---|
| **Système** | macOS 10.15 (Catalina) ou plus récent |
| **Processeur** | Apple Silicon (builds `aarch64` publiées ici) |
| **Connexion** | Requise uniquement pour les mises à jour et certaines icônes de services |

---

## Contenu d'une release

Chaque version publiée contient typiquement :

| Fichier | Usage |
|---------|-------|
| `SubTracker_X.X.X_aarch64.dmg` | Installateur pour une première installation |
| `SubTracker_aarch64.app.tar.gz` | Archive utilisée par la mise à jour in-app |
| `SubTracker_aarch64.app.tar.gz.sig` | Signature cryptographique de l'archive |
| `latest.json` | Manifeste Tauri Updater (version, URL, signature) |

Les releases sont produites automatiquement par GitHub Actions depuis le dépôt source privé, puis publiées ici.

---

## Confidentialité

SubTracker ne collecte aucune donnée personnelle. Les abonnements et paramètres sont stockés **localement sur votre Mac** — aucune synchronisation cloud, aucun compte utilisateur.

Ce dépôt sert uniquement à distribuer l'application et ses mises à jour. Aucune donnée d'utilisation n'est transmise lors du téléchargement ou de la vérification de version.

---

## Signaler un problème

Pour un bug, une suggestion ou une question sur l'application, ouvrez une [issue](https://github.com/mvsko/subtracker-releases/issues) sur ce dépôt.

Indiquez la version de SubTracker, votre version de macOS et, le cas échéant, le fichier téléchargé (`.dmg` ou mise à jour in-app).

---

## Licence

SubTracker est distribué sous licence MIT.
