# Site Web Ventousage Cinéma

Site web statique professionnel pour une entreprise de ventousage spécialisée dans la réservation de stationnement pour tournages de films et productions audiovisuelles.

## 🎬 Description

Ce site présente les services de Ventousage Cinéma, une entreprise spécialisée dans la sécurisation des espaces de stationnement lors de tournages cinématographiques. Le site comprend 5 pages principales avec un design moderne, responsive et professionnel.

## 📁 Structure du Projet

```
ventousage-cinema-site/
├── index.html              # Page d'accueil
├── services.html            # Page des services détaillés
├── realisations.html        # Galerie des réalisations
├── contact.html             # Page de contact avec formulaire
├── mentions.html            # Mentions légales
├── assets/
│   ├── css/
│   │   └── style.css        # Styles CSS principaux
│   └── js/
│       └── main.js          # JavaScript pour le menu burger
├── README.md                # Documentation du projet
└── todo.md                  # Suivi du développement
```

## 🎨 Caractéristiques du Design

### Palette de Couleurs
- **Fond principal** : Blanc (#ffffff)
- **Texte** : Noir/Gris foncé (#1e293b)
- **Couleur d'accent** : Bleu (#2563eb)
- **Couleur secondaire** : Orange (#f97316)

### Typographie
- **Police principale** : Segoe UI, Tahoma, Geneva, Verdana, sans-serif
- **Hiérarchie** : Titres en gras, texte lisible et aéré
- **Responsive** : Adaptation automatique sur mobile

### Design Responsive
- **Desktop** : Navigation horizontale, grilles multi-colonnes
- **Mobile** : Menu burger, colonnes uniques, boutons pleine largeur
- **Breakpoints** : 768px et 480px

## 📱 Fonctionnalités

### Navigation
- Menu de navigation fixe en haut de page
- Menu burger automatique sur mobile
- Liens actifs mis en surbrillance
- Smooth scrolling pour les ancres

### Pages
1. **Accueil** : Présentation, services clés, avantages
2. **Services** : Détail complet des prestations
3. **Réalisations** : Galerie d'images avec overlay
4. **Contact** : Formulaire Netlify + informations pratiques
5. **Mentions** : Informations légales

### Formulaire de Contact
- **Compatible Netlify** : `data-netlify="true"`
- **Champs requis** : Nom, Email, Téléphone
- **Champs optionnels** : Société, Type de projet, Adresse, Dates, Message
- **Protection spam** : Honeypot intégré
- **Validation** : HTML5 native

## 🚀 Installation et Utilisation

### Prérequis
- Navigateur web moderne
- Serveur web local (optionnel pour le développement)

### Lancement Local
```bash
# Avec Python 3
python3 -m http.server 8000

# Avec Node.js
npx serve .

# Avec PHP
php -S localhost:8000
```

Puis ouvrir : `http://localhost:8000`

### Déploiement
Le site est prêt pour le déploiement sur :
- **Netlify** (recommandé pour le formulaire)
- **Vercel**
- **GitHub Pages**
- **Serveur web classique**

## 📋 Formulaire Netlify

Le formulaire de contact est configuré pour Netlify avec :
- `data-netlify="true"` sur le formulaire
- `name="contact"` pour l'identification
- Champ honeypot anti-spam
- Tous les champs nommés correctement

## 🛠️ Technologies Utilisées

- **HTML5** : Structure sémantique
- **CSS3** : Variables CSS, Flexbox, Grid, Media Queries
- **JavaScript** : Menu burger, navigation active
- **Netlify Forms** : Traitement des formulaires

## 📱 Compatibilité

- **Navigateurs** : Chrome, Firefox, Safari, Edge (versions récentes)
- **Appareils** : Desktop, Tablette, Mobile
- **Résolutions** : De 320px à 1920px+

## 🎯 Optimisations

### Performance
- CSS et JS minifiés en production
- Images optimisées (placeholders utilisés)
- Chargement rapide des polices système

### SEO
- Balises meta complètes
- Structure HTML sémantique
- URLs propres et descriptives
- Alt text pour les images

### Accessibilité
- Contraste suffisant (WCAG AA)
- Navigation au clavier
- Labels de formulaire appropriés
- Structure de titres logique

## 📝 Personnalisation

### Couleurs
Modifier les variables CSS dans `assets/css/style.css` :
```css
:root {
    --color-primary: #2563eb;
    --color-secondary: #f97316;
    /* ... autres couleurs */
}
```

### Contenu
- Remplacer les textes dans les fichiers HTML
- Ajouter de vraies images dans `assets/images/`
- Compléter les mentions légales avec les vraies informations

### Formulaire
- Modifier les champs dans `contact.html`
- Configurer Netlify pour recevoir les soumissions
- Personnaliser les messages de confirmation

## 📞 Support

Pour toute question ou modification :
- Email : contact@ventousage-cinema.fr
- Téléphone : 01 23 45 67 89

## 📄 Licence

Tous droits réservés - Ventousage Cinéma 2025

---

**Développé avec ❤️ pour Ventousage Cinéma**

