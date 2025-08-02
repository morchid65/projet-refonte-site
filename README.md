# 🧠 Projet Web – Wu Tao Academy

Ce projet représente une approche progressive de la création d’un site web modulaire, stylisé, et optimisé pour le responsive. Il illustre un véritable cheminement technique, depuis des échecs initiaux jusqu’à une solution maîtrisée et documentée.

---

## 🔧 Fonctionnalités clés

### 💡 Injection du Header avec Fetch

html
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
```

- `depth2` : calcule le niveau de profondeur du fichier actuel
- `fetch()` : charge dynamiquement le header
- Modularisation : réutilisation du même composant `header.html`

---

### 📥 Injection du Footer

html
<div id="footer-container"></div>
<script>
  fetch('/footer.html')
    .then(res => res.text())
    .then(html => {
      document.getElementById('footer-container').innerHTML = html;
    });
</script>
```

- Centralisation du footer → une seule source pour toutes les pages

---

### 🎨 Style CSS pour image centrée

```css
.image-centre {
  background-color: rgb(168, 164, 164);
  box-shadow: 5px 5px 10px #222;
  border: solid 20px rgb(107, 107, 107);
}
```

- Style visuel avec ombrage & encadrement personnalisé

---

### 🔐 Validation de mot de passe

html
<input type="password" id="Mot-de-Passe" placeholder="Mot de passe">
<button id="submit-password">OK</button>

<script>
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
</script>


- Sécurité de base pour bloquer l’accès à certaines sections

---

### 🖼️ Carrousel interactif (galerie)

javascript
const images = [...]; // Tableau d’URLs
function showImage(index) {
  if (images[index]) {
    mainImg.style.opacity = 0;
    setTimeout(() => {
      mainImg.src = images[index];
      mainImg.style.opacity = 1;
    }, 200);
  }
}

leftArrow.addEventListener("click", () => {
  currentIndex = (currentIndex - 1 + images.length) % images.length;
  showImage(currentIndex);
});

- Galerie avec transitions fondues et navigation fluide

---

## 📌 Difficultés rencontrées

- Conflits de classes CSS → résolus via `.img-base`
- Sections peu responsive → correction avec **Flexbox**
- Navigation instable → réglée via composants injectés
- Tentative initiale de tout centraliser → trop lourd à maintenir

---

## ✔️ Solutions techniques

- 🔧 Séparation des composants HTML (`header.html`, `footer.html`)
- 🎨 CSS fragmenté en fichiers thématiques
- 🧪 Tests manuels sur chaque inclusion JS / responsive
- 📁 Organisation claire des fichiers, logique modulaire

---

## 🔁 Déroulement du Développement

### 🧨 Échecs & Transition

> “Le Plan B consistait à tout réunir — mais c’était une impasse.”

- Trop de contenu → surcharge
- CSS ingérable, navigation fragile
- Résultat : instabilité et confusion

---

### ✨ Rebirth avec Plan C

> “Une fois que le header a fonctionné, tout a changé.”

- Granularité → fichiers spécifiques par rôle
- Création de `header.html` et `footer.html` modulaires
- Structuration parent-enfant optimisée
- Fragmentation du CSS pour lisibilité
- Responsive system mis en place manuellement

---

### 🧠 Intelligence du Plan C – IA + Reprise manuelle

| Étape        | Action                              |
|--------------|--------------------------------------|
| 🟡 Extraction | Séparation HTML par section          |
| 🔵 Structuration | Forme optimisée par IA               |
| 🔴 Reprise     | Relecture et corrections manuelles   |
| 🟢 Stylisation | Application ciblée du design         |

---

## 📘 Posture finale

Ce projet n’est pas simplement un site.  
C’est un **dojo numérique**, une trace d’évolution, le reflet d’un apprentissage **technique et personnel**.

> “Je ne voulais pas juste créer un site fonctionnel.  
> Je voulais apprendre à mieux coder, à résoudre les problèmes, à maîtriser chaque étape.”

---

## 🙏 Remerciements

Merci à mon encadrant, à l’équipe, à l’IA…  
…et aux bugs, qui m’ont forcé à devenir meilleur.

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Documentation Technique – Wu Tao Academy</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 2rem; background-color: #fdfdfd; color: #222; }
    h1, h2 { color: #444; }
    pre { background: #eee; padding: 1rem; overflow-x: auto; border-left: 5px solid #ccc; }
    ul { padding-left: 1.5rem; margin-bottom: 2rem; list-style-type: disc; }
    ul li { margin-bottom: 0.5rem; }
    ul ul { list-style-type: circle; }
    section { margin-bottom: 3rem; padding: 1rem; background-color: #fafafa; border: 1px solid #ddd; border-radius: 8px; }
    code { font-family: Consolas, monospace; }
    img { width: 100%; margin-bottom: 1rem; border-radius: 8px; box-shadow: 0 0 6px #aaa; }
    h2 { border-bottom: 2px solid #ccc; padding-bottom: 0.3rem; margin-top: 0; }
  </style>
</head>
<body>

<h1>📘 Documentation Technique – Wu Tao Academy</h1>

<!-- SECTION INJECTION HEADER -->
<section>
  <h2>📦 Injection du Header (modularisation)</h2>
  <img src="header.png" alt="Aperçu du Header injecté" style="width:25%; display:block; margin:0 auto;">
  <img src="header2.png" alt="Aperçu du Header injecté">
  <pre><code>
&lt;script&gt;
  const depth2 = location.pathname.split('/').length - 2;
  const path2 = '../'.repeat(depth2) + 'header.html';
  fetch(path2)
    .then(response =&gt; response.text())
    .then(data =&gt; {
      document.getElementById('header-container').innerHTML = data;
    })
    .catch(error =&gt; console.error('Erreur chargement header:', error));
&lt;/script&gt;
  </code></pre>
  <ul>
    <li><strong>depth2</strong> : calcule la profondeur du fichier</li>
    <li><strong>fetch()</strong> : charge dynamiquement le fichier `header.html`</li>
    <li><strong>Modularisation</strong> : permet un code plus propre et réutilisable</li>
  </ul>
</section>

<!-- SECTION FOOTER -->
<section>
  <h2>📥 Injection du Footer</h2>
  <img src="footer.png" alt="Aperçu du Footer injecté">
  <pre><code>
&lt;div id="footer-container"&gt;&lt;/div&gt;
&lt;script&gt;
  fetch('/footer.html')
    .then(res =&gt; res.text())
    .then(html =&gt; {
      document.getElementById('footer-container').innerHTML = html;
    });
&lt;/script&gt;
  </code></pre>
  <p>Injection dynamique du footer pour centraliser la mise à jour.</p>
</section>

<!-- SECTION AUDIO -->
<section>
  <h2>🎧 Bouton Audio (lecture/pause)</h2>
  <img src="LIEN_IMAGE_AUDIO.png" alt="Bouton audio affiché">
  <pre><code>
&lt;button id="audio-toggle"&gt;&lt;span class="icon"&gt;&lt;/span&gt;&lt;/button&gt;
&lt;audio id="footer-audio" src="chemin/vers/audio.mp3"&gt;&lt;/audio&gt;

&lt;script&gt;
  const toggleBtn = document.getElementById('audio-toggle');
  const audio = document.getElementById('footer-audio');
  let isPlaying = false;

  toggleBtn.addEventListener('click', () =&gt; {
    isPlaying = !isPlaying;
    if (isPlaying) {
      audio.play().catch(() =&gt; {});
      toggleBtn.classList.add('playing');
    } else {
      audio.pause();
      toggleBtn.classList.remove('playing');
    }
  });
&lt;/script&gt;
  </code></pre>
</section>

<!-- SECTION MOT DE PASSE -->
<section>
  <h2>🔐 Validation du mot de passe</h2>
  <img src="formulaire-mot-de-passe.png" alt="Formulaire de mot de passe affiché">
  <pre><code>
&lt;input type="password" id="Mot-de-Passe" placeholder="Mot de passe"&gt;
&lt;button id="submit-password"&gt;OK&lt;/button&gt;

&lt;script&gt;
document.querySelector("#submit-password").addEventListener("click", function() {
  let passwordInput = document.getElementById("Mot-de-Passe").value;
  if (passwordInput === "") {
    alert("Veuillez saisir un mot de passe.");
  } else if (passwordInput.length &lt; 6) {
    alert("Le mot de passe doit contenir au moins 6 caractères.");
  } else {
    alert("Mot de passe valide !");
  }
});
&lt;/script&gt;
  </code></pre>
</section>

<!-- SECTION GALERIE -->
<section>
  <h2>🖼️ Script Carrousel – Galerie interactive</h2>
  <img src="image-caroussel.png" alt="Carrousel interactif affiché">
  <img src="caroussel-img.png" alt="Carrousel interactif affiché">
  <pre><code>
const images = [...]; // Tableau d’URLs
function showImage(index) {
  if (images[index]) {
    mainImg.style.opacity = 0;
    setTimeout(() =&gt; {
      mainImg.src = images[index];
      mainImg.style.opacity = 1;
    }, 200);
  }
}

leftArrow.addEventListener("click", () =&gt; {
  currentIndex = (currentIndex - 1 + images.length) % images.length;
  showImage(currentIndex);
});
  </code></pre>
</section>

<!-- SECTION README EN MARKDOWN -->
<section>
  <h2>📒 README – Projet Web Wu Tao Academy</h2>
  <pre><code>
# 🧠 Projet Web – Injection Dynamique & Modularisation

Ce projet représente une approche progressive de la création d’un site web modulaire, stylisé, et optimisé pour le responsive.

## 🔧 Fonctionnalités clés

...

## 🙏 Remerciements

Merci à mon encadrant, à l’équipe, à l’IA…  
…et aux bugs, qui m’ont forcé à devenir meilleur.
  </code></pre>
</section>

</body>
</html>
