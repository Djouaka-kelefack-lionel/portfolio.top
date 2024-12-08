

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
   └── /img
       ├── profile.jpg
       ├── logo.png
       └── /projects
   ```
3. **Lancez le site** en ouvrant `index.html` dans votre navigateur.

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

