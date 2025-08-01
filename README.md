# 🧧 README – Projet Refonte Site Wu Tao Academy

[![Statut du Projet](https://img.shields.io/badge/Statut-En%20Cours%20(Phénix)-orange)]()
[![Méthodologie](https://img.shields.io/badge/Méthodologie-Agile%20&%20Résiliente-blue)]()
[![Compétence](https://img.shields.io/badge/Compétence-Résolution%20de%20Problèmes-red)]()
[![Dojo de Progression](https://img.shields.io/badge/Dojo-Progression%20Continue-black)]()

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)]()
[![Flexbox](https://img.shields.io/badge/Layout-Flexbox-green)]()
[![Fetch API](https://img.shields.io/badge/Fetch%20API-JavaScript-yellow)]()
[![Responsive](https://img.shields.io/badge/Layout-Responsive-green)]()
[![Collaboration IA](https://img.shields.io/badge/Collaboration-IA%20&%20Manuelle-lightgrey)]()

---

## 📚 Sommaire

- [📌 Contexte & Philosophie du Projet](#-contexte--philosophie-du-projet)
- [🔁 Déroulement du Développement](#-déroulement-du-développement)
- [🗂️ Structure & Code](#️-structure--code)
- [📊 Analyse & Résolution](#-analyse--résolution)
- [🎥 Vidéo de Présentation](#-vidéo-de-présentation)
- [📘 Parcours personnel & apprentissage technique](#-parcours-personnel--apprentissage-technique)
- [🔮 À venir & Remerciements](#-à-venir--remerciements)

---

## 📘 Parcours personnel & apprentissage technique

Ce projet est né du chaos : un site désorganisé, des chemins cassés, un CSS en vrac. Mais c’est précisément dans cette situation que la progression est devenue essentielle. À force de tentatives, d’échecs, de reprises IA et de code à la main, chaque fichier est devenu un symbole d'apprentissage.

> “Je ne voulais pas tricher ni faire semblant.  
> J’ai voulu comprendre chaque partie en la codant moi-même.”

🎯 Objectifs techniques atteints :
- Refonte totale du header et footer en modules injectés
- Structuration parent-enfant optimisée
- Fragmentation du CSS pour lisibilité
- Système responsive sur l’ensemble du site
- Création manuelle d’éléments HTML

🧠 IA + manuel :
- IA pour organiser, mais chaque ligne reprise et corrigée manuellement
- Bugs transformés en leçons : +30 résolus et documentés

Ce README est à l’image du site : un dojo numérique, une trace de montée en compétence.

---

# 📄 Documentation Technique – Wu Tao Academy

 html
<h2>Injection du Header avec Fetch</h2>
<pre><code>
<script>
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

<h2>Extrait CSS pour une image stylisée</h2>
<pre><code>
.image-centre {
  background-color: rgb(168, 164, 164);
  box-shadow: 5px 5px 10px #222;
  border: solid 20px rgb(107, 107, 107);
}
</code></pre>

<h2>💡 Explication</h2>
<ul>
  <li><strong>depth2</strong> : calcule le niveau de profondeur du fichier actuel</li>
  <li><strong>fetch()</strong> : charge le header dynamiquement</li>
  <li><strong>image-centre</strong> : applique un style visuel + ombrage</li>
</ul>

<h2>📌 Difficultés rencontrées</h2>
<ul>
  <li>Conflits de classes CSS résolus par standardisation (.img-base)</li>
  <li>Responsive complexe sur certaines sections → réglé avec Flexbox</li>
  <li>Navigation instable corrigée via modules HTML injectés</li>
</ul>

<h2>✔️ Solutions techniques</h2>
<ul>
  <li>Séparation de chaque composant HTML</li>
  <li>CSS fragmenté en fichiers thématiques</li>
  <li>Test manuel systématique sur chaque inclusion JS / navigation</li>
</ul>
