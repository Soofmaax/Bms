# Stratégie de Gestion Multilingue pour un Site Statique

## Introduction

Ce document détaille les meilleures pratiques et les approches recommandées pour rendre un site web statique multilingue. L'objectif est de permettre au site 'Ventousage Cinéma' de s'adresser à un public international, notamment les boîtes de production étrangères, en offrant une expérience utilisateur fluide dans différentes langues.

## 1. Approches Générales pour les Sites Multilingues Statiques

Il existe plusieurs méthodes pour gérer le contenu multilingue sur un site statique. Le choix dépend de la complexité du site, du nombre de langues cibles, et des outils disponibles.

### 1.1. Duplication Complète du Site (Dossiers ou Sous-domaines)

Cette approche consiste à créer une copie complète du site pour chaque langue. Par exemple :
- `monsite.com/fr/` pour le français
- `monsite.com/en/` pour l'anglais
- `en.monsite.com` pour l'anglais (sous-domaine)

**Avantages :**
- Simplicité de mise en œuvre pour les petits sites.
- Très bon pour le SEO (chaque version linguistique est traitée comme un site distinct).
- Facile à héberger sur des plateformes statiques.

**Inconvénients :**
- Maintenance lourde : toute modification de structure ou de design doit être appliquée à chaque copie du site.
- Gestion des traductions manuelle et sujette aux erreurs.

### 1.2. Utilisation de Fichiers de Données (JSON/YAML) avec un Générateur de Site Statique (SSG)

Cette méthode implique de stocker le contenu textuel de chaque langue dans des fichiers de données séparés (par exemple, des fichiers JSON ou YAML). Un générateur de site statique (comme Jekyll, Hugo, Eleventy, Next.js, Gatsby) utilise ensuite ces données pour générer les pages HTML pour chaque langue.

**Avantages :**
- Séparation claire du contenu et de la structure.
- Facilite la gestion des traductions (les traducteurs travaillent uniquement sur les fichiers de données).
- Réduit la duplication de code HTML/CSS.
- Très efficace pour les sites de taille moyenne à grande.

**Inconvénients :**
- Nécessite l'utilisation d'un SSG, ce qui ajoute une étape de build au processus de déploiement.
- Courbe d'apprentissage pour la configuration du SSG.

### 1.3. JavaScript pour la Traduction Côté Client

Cette approche charge toutes les traductions dans le navigateur et utilise JavaScript pour basculer dynamiquement le contenu de la page en fonction de la langue sélectionnée. Des bibliothèques comme `i18next` ou `react-i18next` sont couramment utilisées.

**Avantages :**
- Très flexible et dynamique.
- Pas de duplication de pages HTML.
- Idéal pour les applications web monopages (SPA).

**Inconvénients :**
- Moins bon pour le SEO (le contenu n'est pas directement disponible pour les crawlers sans exécution JavaScript).
- Dépendance au JavaScript (si JS est désactivé, la traduction ne fonctionne pas).
- Temps de chargement initial potentiellement plus long si toutes les traductions sont chargées en une fois.

## 2. Recommandation pour 'Ventousage Cinéma'

Compte tenu de la nature du site (statique, relativement peu de pages, besoin de SEO pour les recherches internationales) et de l'objectif d'attirer des boîtes de production étrangères, l'approche de la **duplication complète du site via des dossiers de langue** (`/fr/`, `/en/`) est la plus simple et la plus robuste pour commencer. Elle offre un excellent SEO et une maintenance relativement simple pour un site de cette taille.

Si le site devait évoluer vers des centaines de pages ou de nombreuses langues, l'utilisation d'un SSG serait plus appropriée. Pour l'instant, la duplication manuelle est la plus rapide à mettre en œuvre et à maintenir.

## 3. Étapes pour la Mise en Œuvre (Approche par Dossiers)

### 3.1. Structure des Dossiers

Nous allons créer un dossier par langue à la racine du projet. Par exemple :

```
ventousage-cinema-site/
├── fr/             <-- Contenu français
│   ├── index.html
│   ├── services.html
│   ├── ...
├── en/             <-- Contenu anglais
│   ├── index.html
│   ├── services.html
│   ├── ...
├── assets/
│   ├── css/
│   ├── js/
│   ├── images/
├── ...
```

Le dossier `assets` restera commun à toutes les langues pour éviter la duplication des CSS, JS et images.

### 3.2. Traduction du Contenu

Chaque fichier HTML devra être traduit manuellement pour chaque langue cible. Cela inclut :
- Les titres de page (`<title>`).
- Le texte du header, des sections, du footer.
- Les attributs `alt` des images.
- Les textes des boutons et des liens.
- Les placeholders et labels des formulaires.

### 3.3. Sélecteur de Langue

Un sélecteur de langue simple sera ajouté au header (ou au footer) de chaque page. Il permettra aux utilisateurs de basculer entre les versions linguistiques du site. Ce sélecteur sera un simple lien vers la page équivalente dans l'autre langue.

Exemple :

```html
<div class="language-switcher">
    <a href="/fr/index.html" class="lang-active">FR</a> |
    <a href="/en/index.html">EN</a>
</div>
```

### 3.4. Balises `hreflang` pour le SEO

Pour informer les moteurs de recherche des différentes versions linguistiques d'une page, nous utiliserons la balise `hreflang` dans la section `<head>` de chaque page. Cela aide à éviter les problèmes de contenu dupliqué et à diriger les utilisateurs vers la bonne version linguistique.

Exemple pour `index.html` (version française) :

```html
<link rel="alternate" hreflang="en" href="https://votre-domaine.com/en/index.html" />
<link rel="alternate" hreflang="fr" href="https://votre-domaine.com/fr/index.html" />
<link rel="alternate" hreflang="x-default" href="https://votre-domaine.com/fr/index.html" />
```

`x-default` indique la version par défaut ou de fallback si aucune langue ne correspond à l'utilisateur.

## 4. Outils et Ressources

Pour la traduction, des outils comme `lingo.dev` (mentionné précédemment) peuvent être très utiles pour gérer les chaînes de caractères, même si l'approche est basée sur la duplication de fichiers. Ils peuvent aider à organiser le contenu à traduire.

## Conclusion

La mise en œuvre d'une version multilingue du site 'Ventousage Cinéma' est une étape stratégique pour son développement international. L'approche par duplication de dossiers offre une solution simple, robuste et SEO-friendly pour atteindre cet objectif. Une planification minutieuse de la structure des fichiers et une traduction précise du contenu seront essentielles au succès de cette initiative.

