# Portfolio Website - Navod

Un portfolio moderne développé avec HTML et CSS, mettant en avant des techniques CSS avancées pour créer une expérience utilisateur unique.

## 🎨 Design System

### Couleurs
- **Fond Principal**: `#0a192f` (Bleu foncé)
- **Accent Principal**: `#00b4d8` (Bleu clair)
- **Texte**: 
  - Principal: `#ffffff` (Blanc)
  - Secondaire: `rgba(255, 255, 255, 0.9)`
- **Gradients**:
  - Bordures: `linear-gradient(45deg, #00b4d8, transparent)`
  - Animations: `linear-gradient(315deg, #ff0000, #ffd700, #00ff00)`

### Typographie

css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');
/ Hiérarchie des textes /
h1 { font-size: 4.5rem; }
h2 { font-size: 2.5rem; }
h3 { font-size: 1.8rem; }
p { font-size: 1.1rem; }



## 💫 Animations et Effets

### 1. Animation de Rotation

css
@keyframes rotate {
0% { transform: rotate(0deg); }
100% { transform: rotate(360deg); }
}


Utilisée pour:
- Image de profil
- Bordures lumineuses
- Effets décoratifs

### 2. Effets de Survol


css
.element {
transition: all 0.3s ease;
}
.element:hover {
transform: translateY(-10px);
box-shadow: 0 10px 20px rgba(0, 180, 216, 0.2);
}



### 3. Bordures Lumineuses


css
.element::before {
content: '';
position: absolute;
inset: 0;
border-radius: 20px;
padding: 2px;
background: linear-gradient(45deg, #00b4d8, transparent);
-webkit-mask:
linear-gradient(#fff 0 0) content-box,
linear-gradient(#fff 0 0);
-webkit-mask-composite: xor;
}



## 🎯 Composants Clés

### 1. Image de Profil avec Animation


css
.profile-image {
border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
overflow: hidden;
}
.profile-image::before {
background: linear-gradient(315deg, #ff0000, #ffd700, #00ff00);
animation: rotate 3s linear infinite;
}



### 2. Timeline Verticale


css
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



### 3. Barres de Progression

css
.progress-bar {
background: rgba(0, 180, 216, 0.1);
border: 1px solid rgba(0, 180, 216, 0.3);
overflow: hidden;
}
.progress {
animation: progressAnimation 1.5s ease-out forwards;
}



### 4. Cartes de Service

css
.service-card {
background: rgba(0, 180, 216, 0.05);
border: 1px solid #00b4d8;
transition: all 0.3s ease;
}



## 📱 Techniques Responsive

### Layout Flexbox


css
.container {
display: flex;
justify-content: space-between;
gap: 2rem;
flex-wrap: wrap;
}



### Grilles Adaptatives


css
.grid {
display: flex;
flex-direction: column;
gap: 2rem;
}



## 🎓 Techniques CSS Avancées

### 1. Masques CSS

css
-webkit-mask:
linear-gradient(#fff 0 0) content-box,
linear-gradient(#fff 0 0);
-webkit-mask-composite: xor;



### 2. Pseudo-éléments Créatifs


css
.element::before,
.element::after {
content: '';
position: absolute;
inset: 0;
}



### 3. Animations Personnalisées


css
@keyframes progressAnimation {
from { width: 0; }
}



## 🔧 Optimisations

### Performance
- Utilisation de `transform` pour les animations
- Transitions optimisées avec `will-change`
- Animations hardware-accelerated

### Accessibilité
- Contraste de couleurs optimisé
- Focus states visibles
- Textes lisibles

## 📦 Dépendances

- **FontAwesome** : Icons et éléments graphiques
- **Google Fonts** : Police Poppins
- **Normalize.css** : Reset CSS (recommandé)

## 🚀 Installation et Utilisation

1. Cloner le repository
2. Vérifier la structure des dossiers :
   ```
   /portfolio
   ├── index.html
   ├── style.css
   └── /img
       ├── profile.jpg
       ├── logo.png
       └── projects/
   ```
3. Ouvrir index.html dans un navigateur

## 💡 Bonnes Pratiques CSS

- Organisation modulaire du code
- Variables CSS pour les couleurs et valeurs réutilisables
- Commentaires descriptifs pour les sections complexes
- Nomenclature cohérente
- Optimisation des sélecteurs

## 🔍 Points d'Attention

- Vérifier la compatibilité des navigateurs pour les masques CSS
- Tester sur différents appareils
- Optimiser les images
- Maintenir la cohérence des animations

