# 🧧 README – Projet Refonte Site Wu Tao Academy

[![Statut du Projet](https://img.shields.io/badge/Statut-En%20Cours%20(Phénix)-orange)]()
[![Méthodologie](https://img.shields.io/badge/Méthodologie-Agile%20&%20Résiliente-blue)]()
[![Résolution de Problèmes](https://img.shields.io/badge/Compétence-Résolution%20de%20Problèmes-red)]()
[![Dojo de Progression](https://img.shields.io/badge/Dojo-Progression%20Continue-black)]()

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)]()
[![Flexbox](https://img.shields.io/badge/Layout-Flexbox-green)]()
[![Positionnement CSS](https://img.shields.io/badge/Positionnement-CSS%20Relative-purple)]()
[![Fetch API](https://img.shields.io/badge/Fetch%20API-JavaScript-yellow)]()

[![Collaboration IA](https://img.shields.io/badge/Collaboration-IA%20&%20Manuelle-lightgrey)]()
[![Responsive](https://img.shields.io/badge/Layout-Responsive-green)]()

---

## 📚 Sommaire

- [📌 Contexte & Philosophie du Projet](#-contexte--philosophie-du-projet)
- [🔁 Déroulement du Développement](#-déroulement-du-développement)
  - [🧨 Échecs & Transition](#-échecs--transition)
  - [🔐 Le Header - Noyau Central](#-le-header--noyau-central)
  - [🧠 Intelligence du Plan C](#-intelligence-du-plan-c--ia--reprise-manuelle)
- [🗂️ Structure & Code](#️-structure--code)
  - [📁 Structure du Dossier](#-structure-du-dossier--arborescence-finale)
  - [🎨 Compositions CSS](#-compositions-css-maîtrisées)
  - [📥 Script d’injection dynamique](#-script-dinjection-dynamique)
- [📊 Analyse & Résolution](#-analyse--résolution)
  - [📊 Statistiques Techniques](#-statistiques-techniques--github)
  - [🧵 Résolutions CSS](#-résolutions-css)
- [🎥 Vidéo de Présentation](#-vidéo-de-présentation)
- [🔮 À venir & Remerciements](#-à-venir--remerciements)
  - [🔮 À venir](#-à-venir)
  - [🙏 Remerciements](#-remerciements)
  - [📘 Posture finale](#-posture-finale)


---

## 📌 Contexte & Philosophie du Projet

### Contexte du Projet
Tout a commencé avec un site désorganisé.
Des fichiers éparpillés, des chemins brisés, un CSS difficile à maintenir.
Mais derrière ce chaos, une volonté claire : **comprendre**, **progresser**, **reconstruire**.

### Philosophie de Développement
> “Je n’ai pas voulu tricher avec des raccourcis.
> J’ai voulu apprendre vraiment, en codant chaque partie moi-même.”

- Codage manuel de l’accueil
- Création du menu complet tapé à la main
- Regroupement des éléments visuels
- Structuration assistée par IA → reprise manuelle
- Réutilisation des plans échoués comme ressources

---

## 🔁 Déroulement du Développement

### 🧨 Échecs & Transition
#### Plan B échoué
> “Le Plan B consistait à tout réunir — mais c’était une impasse.”

- Trop de contenu → surcharge
- CSS ingérable, navigation fragile
- Résultat : instabilité et confusion

#### Rebirth avec Plan C
- Granularité → fichiers spécifiques par rôle
- Création de `header.html` et `footer.html` modulaires

### 🔐 Le Header – Noyau central
> “Une fois que le header a fonctionné, tout a changé.”

- Fusion `<head>` / `<header>` provoquait des bugs
- Résolution :
  - Séparation structurée
  - Chargement dynamique via `fetch()`
  - Navigation rétablie + stylisation fluide

### 🧠 Intelligence du Plan C – IA + Reprise manuelle
> “J’ai extrait, structuré avec l’IA, et repris chaque ligne moi-même.”

| Étape | Action |
| --- | --- |
| 🟡 Extraction | Séparation HTML par section |
| 🔵 Structuration | Forme optimisée par IA |
| 🔴 Reprise | Relecture et corrections manuelles |
| 🟢 Stylisation | Application ciblée du design |

---

## 🗂️ Structure & Code

### 📁 Structure du Dossier – Arborescence Finale

WuTaoAcademy/
├── accueil.html
├── header.html
├── footer.html
├── README.md
├── note projet.md
├── css/
│   ├── global.css
│   ├── competition.css
│   ├── plus.css
│   └── responsive.css
├── Sections/
│   ├── agenda.html
│   ├── competitions.html
│   ├── enfants.html
│   └── …
├── Sous-sections/
│   ├── agenda-local.html
│   ├── competitions-1.html
│   ├── enfants-danse.html
│   └── …
├── Img/
│   ├── accueil/
│   ├── competitions/
│   ├── enfants/
│   └── …
└── js/
    └── injectHeaderFooter.js

🎨 Compositions CSS maîtrisées
| Classe CSS | Rôle |
|---|---|
| .container-global | Structure de la page |
| .row, .column | Flexbox pour disposition |
| .side-left, .side-right | Alignements latéraux |
| .image-wrapper | Conteneur d’image modulaire |
| .main-display | Zone d’exposition centrale |
📥 Script d’injection dynamique
> “J’ai extrait, structuré avec l’IA, et repris chaque ligne moi-même.”
> 
<pre><code><script>
const depth2 = location.pathname.split('/').length - 2;
const path2 = '../'.repeat(depth2) + 'header.html';
fetch(path2)
.then(response => response.text())
.then(data => {
document.getElementById('header-container').innerHTML = data;
})
.catch(error => console.error('Erreur chargement header:', error));
</script>
</code></pre>
📊 Analyse & Résolution
📊 Statistiques Techniques & GitHub
<table>
<thead>
<tr>
<th>📌 Indicateur</th>
<th>⚙️ Valeur approximative</th>
</tr>
</thead>
<tbody>
<tr>
<td>🧩 Fichiers HTML créés</td>
<td>90+ (accueil, sections, sous-sections)</td>
</tr>
<tr>
<td>🎨 Fichiers CSS modulaires</td>
<td>4 (global.css, competition.css, plus.css, responsive.css)</td>
</tr>
<tr>
<td>🖼️ Dossiers images organisés</td>
<td>5 (accueil, competitions, enfants, etc.)</td>
</tr>
<tr>
<td>📦 Volume total du projet</td>
<td>≈ 3,4 Mo (en local, avant minification)</td>
</tr>
<tr>
<td>🔁 Refactorisations principales</td>
<td>3 (Plan B → Plan C → Header/Footer modulaires)</td>
</tr>
<tr>
<td>🕰️ Temps de développement estimé</td>
<td>+110h (hors recherches et documentation)</td>
</tr>
<tr>
<td>🤖 Interactions IA</td>
<td>67 sessions (structuration, conseils, bugfixes)</td>
</tr>
<tr>
<td>🧪 Tests manuels effectués</td>
<td>≈ 45+ (navigation, responsive, inclusion JS, etc.)</td>
</tr>
<tr>
<td>📚 Lignes de code tapées</td>
<td>+3 000 (HTML + CSS + JS cumulés)</td>
</tr>
<tr>
<td>🔧 Bugs détectés & résolus</td>
<td>32+ (conflits CSS, chargements dynamiques, erreurs structurelles)</td>
</tr>
</tbody>
</table>
<p><em>“Chaque chiffre est un fragment de l’histoire. Chaque test un pas vers la maîtrise.”</em></p>

### 🧵 Résolutions CSS

| ❌ Erreur rencontrée | ✅ Solution mise en place |
|---|---|
| Classes en double (.img1, .img1, etc.) | Classes universelles (.img-base, .container-global) |
| Style injecté au mauvais endroit | Séparation dans fichiers CSS ciblés |
| Mauvais regroupement des images | Containers (.wrapper-img, .row) |
| Positionnement impossible | position: relative + display: flex |
| Casse non respectée (.img-base ≠ .Img-base) | Uniformisation et rigueur syntaxique |
| Fichiers CSS trop lourds | Fragmentation logique (plus.css, etc.) |
| Hiérarchie HTML déstructurée | Structuration parent-enfant optimisée |
> “À chaque bug, une solution. À chaque ligne, une leçon.”


🎥 Vidéo de Présentation
🔗 Visite guidée du site Wu Tao Academy – Youtube
🔮 À venir & Remerciements
🔮 À venir
 * 🔄 Finalisation de la section “Plus” avec carousel responsive
 * 🖌️ Création d’une version HTML stylisée du README
 * 🌍 Traduction en anglais pour portfolio international
 * 📄 Ajout d’un système de composants réutilisables
   
### 🙏 Remerciements

Ce projet n’aurait jamais existé sans le stage que j’ai pu effectuer — C’est grâce à cette
opportunité, à ce cadre, à cet encadrement que j’ai pu progresser autant.
Je remercie sincèrement mon encadrant et l’environnement du stage, car il a été le
catalyseur de cette transformation technique et personnelle.
Merci aussi à l’IA pour son rôle d’architecte silencieux, et à tous les bugs, erreurs… qui
m’ont rendu meilleur à chaque ligne de code.

### 📘 Posture finale

Ce projet n’est pas qu’un site.
C’est un dojo de progression, une trace d’apprentissage.
> Ce site, ce projet, ce README… tout est le fruit d’une démarche personnelle d’apprentissage.
> Je ne voulais pas juste créer un site fonctionnel.
> Je voulais apprendre à mieux coder, à résoudre les problèmes, à maîtriser chaque étape.
> Chaque fichier que j’ai structuré est un symbole de progression.
> Ce dojo numérique est mon espace d’évolution.
