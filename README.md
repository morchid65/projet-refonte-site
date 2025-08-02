# 🐉 Projet Wu Tao Academy – Site Web HTML/CSS/JS

---

## 📘 Sommaire

- [🎓 Présentation du projet](#présentation-du-projet)
- [📽️ Vidéos de démonstration](#vidéos-de-démonstration)
- [🚀 Progression technique personnelle](#progression-technique-personnelle)
- [🛠️ Difficultés rencontrées & solutions](#difficultés-rencontrées--solutions)
- [📊 Statistiques GitHub](#statistiques-github)
- [🧠 Architecture et organisation des fichiers](#architecture-et-organisation-des-fichiers)
- [🔧 Exemples de scripts JavaScript](#exemples-de-scripts-javascript)
- [🎨 Extrait du code CSS du menu général](#extrait-du-code-css-du-menu-général)
- [⏳ Avant / Après – Évolution du menu](#avant--après--évolution-du-menu)
- [🧩 Idées d'amélioration](#idées-damélioration)
- [🙏 Remerciements](#remerciements)
- [📚 Résumé pédagogique](#résumé-pédagogique)

---

## 🎓 Présentation du projet

Site web vitrine pour une école d’arts martiaux. Réalisé en HTML, CSS, JavaScript — sans framework. L’objectif est de structurer un code modulaire et maintenable, intégrer dynamiquement les composants (`header`, `footer`), et offrir une navigation fluide à travers des sections/sous-sections.

---

### 🏠 Présentation générale du site
🎥 [Voir la vidéo](videos/presentation-site.mp4)  
_Aperçu du site terminé, navigation principale, esthétisme._

### 🧩 Présentation du Header, Footer, Accueil + fichier HTML et CSS
🎥 [Voir la vidéo](videos/integration-header-footer.mp4)  
_Modularisation du layout avec JS + découpage CSS._

### 📂 Structure du projet
🎥 [Voir la vidéo](videos/structure-arborescence.mp4)  
_Organisation des fichiers et logique technique._


> _⚠️ Vidéos sans son mais très visuelles. Durée moyenne : 5 min._

---

## 🚀 Progression technique personnelle

| Phase            | Description |
|------------------|-------------|
| 🐣 Départ         | 1 semaine pour 2 fichiers. Utilisation de l’IA et fiche CSS commentée pour apprendre |
| 🌱 Milieu         | Compréhension progressive, erreurs multiples (class dupliquées, marges abusives, etc.) |
| 🔥 Apogée         | Création rapide, classes réutilisables, injection dynamique, raffinement du style |
| ⚒️ Révision finale | Tour complet des fichiers, optimisation CSS, rendu cohérent et professionnel |

> Temps de création d’un fichier CSS : de plusieurs jours → quelques minutes (1 à 20 min selon complexité)

---

## 🛠️ Difficultés rencontrées & solutions

| 🧩 Problème | ✅ Solution |
|------------|-------------|
| Erreurs de chemin d'image | Nommage strict, capture ciblée, test par lien direct |
| Margin excessive / Position relative | Refactoring complet, classes de positionnement créées |
| InjectHeader déplaçait les fichiers | Séparation du header, script `depth2` intelligent |
| Header fusionné avec DOCTYPE | Restructuration : HTML nettoyé et modularisé |
| CSS dans un seul fichier trop long | Fragmentation CSS par page et par logique visuelle |

---

## 📊 Statistiques GitHub

| 🔢 Métrique | Valeur (estimée) |
|------------|------------------|
| 🗂️ Nombre de fichiers HTML | ~100 |
| 🎨 Fichiers CSS | 10+ |
| ⏱️ Temps total estimé | +100 heures |
| 🔄 Commits | 60 à 100 |
| 🧠 Apprentissage IA | Intense en début, autonomie progressive |

## 📊 Statistiques GitHub & WakaTime

…Stats GitHub ici…

[![wakatime](https://wakatime.com/badge/user/3d07be02-2a28-4eec-96eb-751c50769ce3/project/815baf83-8831-4339-845c-df23def8ea2b.svg)](https://wakatime.com/badge/user/3d07be02-2a28-4eec-96eb-751c50769ce3/project/815baf83-8831-4339-845c-df23def8ea2b)

### 🧭 Suivi WakaTime (semaine 1)
![Graph](graph-wakatime.png)

*(Activité sur 7 jours)*

---

## 🧠 Architecture et organisation des fichiers

```plaintext
WuTaoAcademy/
├── accueil.html
├── header.html
├── footer.html
├── README.md
├── Documentation.html
├── Sections/
├── Sous-sections/
├── css/
│   ├── accueil-header-css/
│   ├── section-css/
│   ├── sous-sections-css/
├── Img/
│   └── img-doc/
├── js/
│   └── injectHeaderFooter.js
```

---

## 🔧 Exemples de scripts JavaScript

### 📦 Injection du Header
![Header injecté](header.png)
![Header version 2](header2.png)

```js
const depth2 = location.pathname.split('/').length - 2;
const path2 = '../'.repeat(depth2) + 'header.html';
fetch(path2)
  .then(response => response.text())
  .then(data => {
    document.getElementById('header-container').innerHTML = data;
  });
```

### 📥 Injection du Footer
![Footer](footer.png)

```js
fetch('/footer.html')
  .then(res => res.text())
  .then(html => {
    document.getElementById('footer-container').innerHTML = html;
  });
```

### 🔐 Formulaire mot de passe
![Mot de passe](formulaire-mot-de-passe.png)

```js
document.querySelector("#submit-password").addEventListener("click", function() {
  let passwordInput = document.getElementById("Mot-de-Passe").value;
  if (passwordInput === "") {
    alert("Veuillez saisir un mot de passe.");
  } else if (passwordInput.length < 6) {
    alert("Le mot de passe doit contenir au moins 6 caractères.");
  } else {
    alert("Mot de passe valide !");
  }
});
```

### 🖼️ Carrousel images
![Carrousel](image-caroussel.png)
![Carrousel img](caroussel-img.png)

```js
function showImage(index) {
  if (images[index]) {
    mainImg.style.opacity = 0;
    setTimeout(() => {
      mainImg.src = images[index];
      mainImg.style.opacity = 1;
    }, 200);
  }
}
```

---

## 🎨 Extrait du code CSS du menu général

```css
.Menu {
  width: 1700px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  padding: 0 20px;
  background: #f5f5f5;
}

.Menu > li {
  position: relative;
  padding: 15px 30px;
  font-family: Arial;
  font-size: 20px;
  font-weight: bold;
  cursor: pointer;
}

.Menu > li:hover {
  background: #222;
  color: #fff;
}

.Menu > li > ul {
  position: absolute;
  top: 100%;
  left: 0;
  background: #f5f5f5;
  display: none;
}

.Menu > li:hover > ul {
  display: block;
}
```

---

## ⏳ Avant / Après – Évolution du menu

### 🔁 Ancienne version (HTML brut)
```html
<li>Agenda
  <ul>
    <li>Décembre 2022</li>
    ...
  </ul>
</li>
```

### 🚀 Version actuelle (structure dynamique)
```html
<li><a href="/sections/agenda.html">Agenda</a>
  <ul>
    <li><a href="/sous-sections/agenda/decembre-2022.html">Décembre 2022</a></li>
    ...
  </ul>
</li>
```

---

## 🧩 Idées d'amélioration

- 🧠 Créer un **fichier CSS unique** avec classes réutilisables (h1, p, flex, grid)
- 📂 Commenter chaque section proprement et structurer par type de style
- 🤖 Script qui crée des blocs HTML dynamiques à partir de layouts prédéfinis
- 🔗 Script qui automatise le lien relatif des fichiers CSS/header/footer selon profondeur
- ⚙️ Rendu final : structure unifiée, logique modulaire, plus rapide et maintenable

---

## 🙏 Remerciements

Un grand merci à mon professeur, à ceux qui m'ont soutenu, et aux outils qui m'ont permis de grandir.  
Merci aux bugs qui ont réveillé ma rigueur, et à l’IA pour m’avoir donné les clés — que j’ai fini par maîtriser tout seul.

---

## 📚 Résumé pédagogique

> Ce README reflète mon parcours : de débutant dépendant à un développeur autonome et structuré.  
> J'ai appris à coder, organiser, corriger, maintenir — mais surtout à penser et décider.
