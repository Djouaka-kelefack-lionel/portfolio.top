

# **Portfolio Website - LeoDev**

Un portfolio moderne et minimaliste mettant en avant des techniques **CSS avancées** et des animations uniques pour offrir une expérience utilisateur immersive. Ce projet, développé avec **HTML** et **CSS**, allie esthétique et performance.

---

## 🎨 **Design System**

### Couleurs
- **Fond Principal** : `#0a192f` (Bleu foncé élégant)
- **Accent Principal** : `#00b4d8` (Bleu lumineux et dynamique)
- **Texte** :
  - Principal : `#ffffff` (Blanc pur)
  - Secondaire : `rgba(255, 255, 255, 0.9)` (Blanc légèrement atténué)
- **Dégradés** :
  - **Bordures** : `linear-gradient(45deg, #00b4d8, transparent)`
  - **Animations** : `linear-gradient(315deg, #ff0000, #ffd700, #00ff00)`

### Typographie
- **Police Principale** : [Poppins](https://fonts.google.com/specimen/Poppins) (Importée depuis Google Fonts)
- **Hiérarchie** :
  ```css
  h1 { font-size: 4.5rem; }
  h2 { font-size: 2.5rem; }
  h3 { font-size: 1.8rem; }
  p { font-size: 1.1rem; }
  ```

---

## 💫 **Animations et Effets**

### 1. Animation de Rotation
Utilisée pour l’image de profil, les bordures lumineuses et les effets décoratifs.

```css
@keyframes rotate {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

### 2. Effets de Survol
Les interactions sont fluides et offrent une rétroaction visuelle captivante.

```css
.element {
  transition: all 0.3s ease;
}
.element:hover {
  transform: translateY(-10px);
  box-shadow: 0 10px 20px rgba(0, 180, 216, 0.2);
}
```

### 3. Bordures Lumineuses
Les bordures dynamiques utilisent des masques CSS pour un effet élégant.

```css
.element::before {
  content: '';
  position: absolute;
  inset: 0;
  border-radius: 20px;
  padding: 2px;
  background: linear-gradient(45deg, #00b4d8, transparent);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
}
```

---

## 🎯 **Composants Clés**

### 1. Image de Profil Animée
```css
.profile-image {
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
  overflow: hidden;
}
.profile-image::before {
  background: linear-gradient(315deg, #ff0000, #ffd700, #00ff00);
  animation: rotate 3s linear infinite;
}
```

### 2. Timeline Verticale
Un design simple et épuré pour afficher les étapes importantes.

```css
.timeline {
  position: relative;
  padding-left: 2rem;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  width: 2px;
  background: #00b4d8;
}
```

### 3. Barres de Progression
Les barres de progression sont animées pour un effet fluide.

```css
.progress-bar {
  background: rgba(0, 180, 216, 0.1);
  border: 1px solid rgba(0, 180, 216, 0.3);
  overflow: hidden;
}
.progress {
  animation: progressAnimation 1.5s ease-out forwards;
}
```

### 4. Cartes de Service
Conçues pour attirer l’attention tout en restant élégantes et professionnelles.

```css
.service-card {
  background: rgba(0, 180, 216, 0.05);
  border: 1px solid #00b4d8;
  transition: all 0.3s ease;
}
```

---

## 📱 **Techniques Responsive**

### **Flexbox pour la Mise en Page**
```css
.container {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  flex-wrap: wrap;
}
```

### **Grilles Adaptatives**
```css
.grid {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}
```

---

## 🎓 **Techniques CSS Avancées**

### 1. Masques CSS
Crée des effets visuels complexes tout en optimisant les performances.

```css
-webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
-webkit-mask-composite: xor;
```

### 2. Pseudo-éléments Créatifs
Utilisés pour les décorations et les animations.

```css
.element::before,
.element::after {
  content: '';
  position: absolute;
  inset: 0;
}
```

### 3. Animations Personnalisées
```css
@keyframes progressAnimation {
  from { width: 0; }
}
```

---

## 🔧 **Optimisations**

### Performance
- **Transform** et **opacity** pour des animations fluides.
- Transitions optimisées avec `will-change`.
- Utilisation de l’accélération matérielle.

### Accessibilité
- Contraste de couleurs soigné pour une meilleure lisibilité.
- États de focus visibles pour la navigation clavier.
- Textes et tailles adaptés pour une accessibilité accrue.

---

## 📦 **Dépendances**

- **FontAwesome** : Icônes élégantes.
- **Google Fonts** : Intégration de la police Poppins.
- **Normalize.css** : Réinitialisation des styles par défaut pour une meilleure compatibilité.

---

## 🚀 **Installation et Utilisation**

1. **Clonez le dépôt** :
   ```bash
   git clone https://github.com/votre-utilisateur/portfolio-website.git
   ```
2. **Vérifiez la structure des fichiers** :
   ```
   /portfolio
   ├── index.html
   ├── style.css
   ├── scrippt.js
   └── /img
       ├── profile.jpg
       ├── logo.png
       └── /projects
   ```


## 📱 **Responsive Design**

### 🌟 **Points de Rupture (Breakpoints)**
Les media queries garantissent une adaptabilité optimale pour tous les dispositifs.

```css
/* TV et grands écrans */
@media screen and (min-width: 1920px) { ... }

/* Tablettes et petits laptops */
@media screen and (max-width: 1024px) { ... }

/* Mobiles */
@media screen and (max-width: 768px) { ... }

/* Petits mobiles */
@media screen and (max-width: 480px) { ... }
```

---

### 🔧 **Variables Responsives**
Les variables facilitent les ajustements de mise en page pour chaque type de dispositif.
```css
:root {
    --padding-mobile: 5%;
    --padding-tablet: 8%;
    --padding-desktop: 10%;
}
```

---

### 🖥️ **Adaptations par Dispositif**

#### **Grands Écrans (>1920px)**
- Police de base augmentée à `18px`.
- Conteneurs plus larges pour utiliser l'espace disponible.
- Espacements optimisés.
```css
html { font-size: 18px; }
.hero-content { max-width: 1000px; }
.projects-container { max-width: 1800px; }
```

#### **Tablettes (≤1024px)**
- Layouts réorganisés en colonnes.
- Images redimensionnées pour une meilleure lisibilité.
- Textes centrés pour une ergonomie accrue.
```css
.hero {
    flex-direction: column;
    text-align: center;
}

.profile-image {
    width: 350px;
    height: 350px;
}
```

#### **Mobiles (≤768px)**
- Menu hamburger avec navigation latérale.
- Empilement vertical des éléments.
- Formulaires adaptés pour des interactions fluides.
```css
.nav-links {
    position: fixed;
    width: 70%;
    height: 100vh;
}

.form-row {
    flex-direction: column;
}
```

#### **Petits Mobiles (≤480px)**
- Réduction des tailles de police.
- Espacements réduits pour maximiser la lisibilité.
- Ajustement des images et des conteneurs.
```css
html { font-size: 13px; }
.profile-image {
    width: 250px;
    height: 250px;
}
```

---

### 📐 **Techniques Responsives Utilisées**

#### **1. Flexbox Responsive**
Dispose les éléments de manière fluide, avec ajustement automatique selon l'espace disponible.
```css
.container {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
}
```

#### **2. Unités Relatives**
- `rem` : tailles de texte relatives à la racine.
- `%` : dimensions adaptatives pour conteneurs.
- `vh/vw` : gestion fluide des hauteurs et largeurs.
- `clamp()` : tailles fluides basées sur des limites.
```css
font-size: clamp(1rem, 2.5vw, 2rem);
```

#### **3. Images Responsives**
Ajustement automatique des images pour s'adapter au conteneur sans perte de qualité.
```css
.profile-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```

#### **4. Grilles Adaptatives**
Création de mises en page dynamiques pour les galeries ou projets.
```css
.project-card {
    flex: 1 1 calc(50% - 1rem);
    min-width: 280px;
}
```

---

### 📱 **Menu Mobile**

#### **Structure HTML**
```html
<div class="menu-toggle">
    <i class="fas fa-bars"></i>
</div>
<div class="nav-links">
    <!-- liens de navigation -->
</div>
```

#### **JavaScript pour le Menu**
Basculer la visibilité du menu mobile tout en évitant les défilements non désirés.
```javascript
menuToggle.addEventListener('click', () => {
    navLinks.classList.toggle('active');
    document.body.style.overflow = navLinks.classList.contains('active') ? 'hidden' : '';
});
```

---

### 🔍 **Tests Responsives**

#### **Dispositifs Testés**
- **Mobiles** : iPhone SE, iPhone 12 Pro, iPhone 12 Pro Max.
- **Tablettes** : iPad Mini, iPad Pro.
- **Bureaux** : Écrans >1920px.

#### **Orientations**
- Portrait : Affichage vertical par défaut.
- Paysage : Ajustements spécifiques pour hauteurs réduites.
```css
@media screen and (max-height: 480px) and (orientation: landscape) {
    .hero { padding-top: 2rem; }
}
```


### 🎯 **Bonnes Pratiques**

1. **Mobile-First** :
   - Conception initiale pour mobiles.
   - Ajout de media queries pour les tailles supérieures.

2. **Performance** :
   - Optimisation des images et fichiers CSS.
   - Chargement conditionnel des ressources lourdes.

3. **Accessibilité** :
   - Contrastes optimisés pour une meilleure lisibilité.
   - Navigation clavier et focus visibles.

4. **Maintenance** :
   - Variables CSS centralisées pour une adaptation rapide.
   - Classes modulaires et réutilisables.

---

   
5. **Lancez le site** en ouvrant `index.html` dans votre navigateur.

---

## 💡 **Bonnes Pratiques CSS**

- Utilisation de **variables CSS** pour garantir la cohérence des styles.
- Organisation modulaire du code pour une maintenance facilitée.
- Sélecteurs optimisés pour réduire la charge du rendu.
- Commentaires détaillés pour les sections complexes.

---

## 🔍 **Points d'Attention**

- Assurez-vous de vérifier la compatibilité des masques CSS sur différents navigateurs.
- Testez le design sur des appareils et tailles d’écran variés.
- Optimisez les images pour améliorer le temps de chargement.
- Maintenez une expérience utilisateur fluide et cohérente.

