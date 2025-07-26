# 🧧 README – Projet Refonte Site Wu Tao Academy

![Stats Wu Tao Academy](https://github.com/morchid65/WuTaoAcademy/raw/main/github-metrics.svg)

## 📚 Sommaire

- [📌 Contexte du Projet](#-contexte-du-projet)  
- [🧠 Philosophie de Développement](#-philosophie-de-développement)  
- [🔁 Échecs & Transition](#-échecs-fondateurs--plan-b-et-transition-stratégique)  
- [🔐 Le Header](#-le-header--noyau-central)  
- [🧠 Intelligence du Plan C](#-intelligence-du-plan-c--ia--reprise-manuelle)  
- [🪨 Structure Technique](#-renaissance-structurelle--nouveau-dossier)  
- [🎨 Compositions CSS](#-compositions-css-maîtrisées)  
- [🧵 Résolutions CSS](#-erreurs-css--résolutions-techniques)
- [🎥 Vidéo de Présentation](#-Vidéo-de-Présentation)  
- [🔮 À venir](#-à-venir)  
- [🙏 Remerciements](#-remerciements)  
- [📘 Posture finale](#-posture-finale)

---

[![Statut du Projet](https://img.shields.io/badge/Statut-En%20Cours%20(Phénix)-orange)]()
[![Méthodologie](https://img.shields.io/badge/Méthodologie-Agile%20&%20Résiliente-blue)]()
[![Résolution de Problèmes](https://img.shields.io/badge/Compétence-Résolution%20de%20Problèmes-red)]()

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)]()
[![Flexbox](https://img.shields.io/badge/Layout-Flexbox-green)]()
[![Positionnement CSS](https://img.shields.io/badge/Positionnement-CSS%20Relative-purple)]()
[![Fetch API](https://img.shields.io/badge/Fetch%20API-JavaScript-yellow)]()

[![Dojo de Progression](https://img.shields.io/badge/Dojo-Progression%20Continue-black)]()
[![Collaboration IA](https://img.shields.io/badge/Collaboration-IA%20&%20Manuelle-lightgrey)]()
[![Responsive](https://img.shields.io/badge/Layout-Responsive-green)]()

---

## 📌 Contexte du Projet

Tout a commencé avec un site désorganisé.  
Des fichiers éparpillés, des chemins brisés, un CSS difficile à maintenir.  
Mais derrière ce chaos, une volonté claire : **comprendre**, **progresser**, **reconstruire**.

---

## 🧠 Philosophie de Développement

> “Je n’ai pas voulu tricher avec des raccourcis.  
> J’ai voulu apprendre vraiment, en codant chaque partie moi-même.”

- Codage manuel de l’accueil  
- Création du menu complet tapé à la main  
- Regroupement des éléments visuels  
- Structuration assistée par IA → reprise manuelle  
- Réutilisation des plans échoués comme ressources  

---

## 🔁 Échecs fondateurs – Plan B et Transition stratégique

### 🧨 Plan B échoué

> “Le Plan B consistait à tout réunir — mais c’était une impasse.”

- Trop de contenu → surcharge  
- CSS ingérable, navigation fragile  
- Résultat : instabilité et confusion  

### 🔁 Rebirth avec Plan C

- Granularité → fichiers spécifiques par rôle  
- Création de `header.html` et `footer.html` modulaires  

---

## 🔐 Le Header – Noyau central

> “Une fois que le header a fonctionné, tout a changé.”

- Fusion `<head>` / `<header>` provoquait des bugs  
- Résolution :
  - Séparation structurée  
  - Chargement dynamique via `fetch()`  
  - Navigation rétablie + stylisation fluide  

---

## 🧠 Intelligence du Plan C – IA + Reprise manuelle

> “J’ai extrait, structuré avec l’IA, et repris chaque ligne moi-même.”

| Étape        | Action                           |
|--------------|----------------------------------|
| 🟡 Extraction | Séparation HTML par section      |
| 🔵 Structuration | Forme optimisée par IA       |
| 🔴 Reprise   | Relecture et corrections manuelles |
| 🟢 Stylisation | Application ciblée du design     |

---

## 🪨 Renaissance structurelle – Nouveau Dossier

- Regroupement propre des éléments  
- Chemins relatifs vérifiés  
- Script JS universel pour `header` et `footer`

```html
<div id="header-container"></div>
<script>
  const depth2 = location.pathname.split('/').length - 2;
  const path2 = '../'.repeat(depth2) + 'header.html';
  fetch(path2)
    .then(response => response.text())
    .then(data => {
      document.getElementById('header-container').innerHTML = data;
    });
</script>
```

---

## 🎨 Compositions CSS maîtrisées

| Classe CSS              | Rôle                          |
|-------------------------|-------------------------------|
| `.container-global`     | Structure de la page          |
| `.row`, `.column`       | Flexbox pour disposition      |
| `.side-left`, `.side-right` | Alignements latéraux       |
| `.image-wrapper`        | Conteneur d’image modulaire   |
| `.main-display`         | Zone d’exposition centrale    |

---

## 🧵 Résolutions CSS

| ❌ Erreur rencontrée                         | ✅ Solution mise en place                               |
|---------------------------------------------|---------------------------------------------------------|
| Classes en double (`.img1`, `.img1`, etc.)  | Classes universelles (`.img-base`, `.container-global`) |
| Style injecté au mauvais endroit            | Séparation dans fichiers CSS ciblés                    |
| Mauvais regroupement des images             | Containers (`.wrapper-img`, `.row`)                    |
| Positionnement impossible                   | `position: relative` + `display: flex`                 |
| Casse non respectée (`.img-base` ≠ `.Img-base`) | Uniformisation et rigueur syntaxique                 |
| Fichiers CSS trop lourds                    | Fragmentation logique (`plus.css`, etc.)               |
| Hiérarchie HTML déstructurée                | Structuration parent-enfant optimisée                  |

> “À chaque bug, une solution. À chaque ligne, une leçon.”

---

## 🔮 À venir

- 🔄 Finalisation de la section “Plus” avec carousel responsive  
- 🖌️ Création d’une version HTML stylisée du README  
- 🌍 Traduction en anglais pour portfolio international  
- 📄 Ajout d’un système de composants réutilisables  

---

## 🙏 Remerciements
Ce projet n’aurait jamais existé sans le stage que j’ai pu effectuer — C’est grâce à cette 
opportunité, à ce cadre, à cet encadrement que j’ai pu progresser autant.

Je remercie sincèrement mon encadrant et l’environnement du stage, car il a été le 
catalyseur de cette transformation technique et personnelle.

Merci aussi à l’IA pour son rôle d’architecte silencieux, et à tous les bugs, erreurs… qui 
m’ont rendu meilleur à chaque ligne de code.

---

## 🔗 Liens utiles

- 📁 [Structure du dossier “Wu Tao Academy”](./WuTaoAcademy/)  
- 📄 [Header modulaire – `header.html`](./header.html)  
- 🧵 [Fichier de style global – `global.css`](./css/global.css)  
- 🎯 [Page Compétition – `competition.html`](./competition.html)  
- ⚙️ [Script d’injection `fetch()` pour header/footer](#🪨-renaissance-structurelle--nouveau-dossier)  
- 📘 [Note projet personnelle – `note projet.md`](./note%20projet.md)

---

## 🎥 Vidéo de Présentation

🔗 [Visite guidée du site Wu Tao Academy – Youtube](https://youtu.be/tonLienIci)

---

## 📘 Posture finale

Ce projet n’est pas qu’un site.  
C’est un **dojo de progression**, une **trace d’apprentissage**.  

---

> Ce site, ce projet, ce README… tout est le fruit d’une démarche personnelle d’apprentissage.  
> Je ne voulais pas juste créer un site fonctionnel.  
> Je voulais apprendre à **mieux coder**, à **résoudre les problèmes**, à **maîtriser chaque étape**.  
> Chaque fichier que j’ai structuré est un symbole de progression.  
> Ce dojo numérique est mon espace d’évolution.
