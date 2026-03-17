# 📋 Pages du Rapport Power BI

Documentation des pages disponibles dans le tableau de bord Power BI "Analyse des Ventes de Jeux Vidéo".

---

## 📍 Page 1 — Vue d'Ensemble (Overview)

### Description
Page d'accueil du tableau de bord offrant une vue globale des performances commerciales de la période sélectionnée.

### Visuels présents

#### 📋 Cards (Cartes de métriques)
- **Coût Total** : Affiche le coüt total d'achat pour la période
- **CA (Chiffre d'Affaires)** : Affiche le CA total en euros
- **Marge Brute** : Différence entre CA et Coüt (CA - Coüt)

**Style :** 
- Fond gris clair
- Polices blanches bold
- Format : XXX,XXM€ ou XXX M€

#### 📥 Carte Bing (Gographie)
- **Titre :** "Distribution géographique des ventes"
- **Coordonnées** : Latitude/Longitude par Pays
- **Bulles** : Tailles proportionnelles aux CA par pays
- **Couleurs** : Gradient bleu (faible) → orange (fort)
- **Interactivité** : Zoom possible, survol affiche le CA du pays

#### 퉰dc️ Slicer (Filtre)
- **Type :** Standard slicer
- **Filtre :** Point de vente (Pays + "En ligne")
- **Position :** Haut droit de la page
- **Mode :** Dropdown ou liste selon version
- **Lien :** Filtre tous les visuels de la page

### Fonctionnalités
- Filtrage par pays pour explorer les données
- Drill-through possible vers Page 2 pour détails par catégorie
- Export PDF / Power Point possible

---

## 📍 Page 2 — Analyse par Catégorie & Année

### Description
Page détaillée permettant l'analyse des ventes par catégories de produits et compétence temporelle (année).

### Visuels présents

#### 📈 Bar Chart (CA par Catégorie)
- **Axe X :** Catégories (Audio, Culture, Électroménagers, Jeux, Ordinateurs, Photo, Smartphones, Vidéo)
- **Axe Y :** CA en euros (format abreuvé : 1.5M€)
- **Couleurs :** Gradient multicolor par catégorie
- **Ordre :** Décroissant (CA le plus élevé d'abord)
- **Interactivité :** Clic pour drill-down par sous-catégorie

#### 📈 Bar Chart Horizontal (CA par Année)
- **Axe Y :** Années (2021, 2022, 2023)
- **Axe X :** CA en euros (format complet)
- **Couleurs :** Trois tons (bleu clair, bleu, bleu foncé) par année
- **Format :** Barres horizontales pour meilleure lisibilité 
- **Labels :** Affichage du CA sur chaque barre
- **Tooltip :** CA, Variation YoY %

#### 🔟 Donut Chart (Répartition CA par Catégorie)
- **Centre :** Logo ou initiales "JV" (Jeux Vidéo)
- **Couronne :** Segments colorés proportionnels au CA
- **Couleurs :** Palette harmonieuse (8 catégories)
- **Labels :** % du CA total ou montant en euros
- **Interactivité :** Clic sur un segment pour filtrer

#### 퉰dc️ Button Slicer (Navigation par Pays)
- **Type :** Button Slicer personnalisé (style tableau de bord professionnel)
- **Pays disponibles :** Allemagne, Australie, Canada, États-Unis, France, Italie, Pays-Bas, Royaume-Uni, En ligne
- **Affichage :** Boutons carrés (ou rectangulaires) avec icones drapeau
- **Style :** Fond clair, texte foncé
- **Sélection active :** Bouton highlighté (couleur différente)
- **Fonction :** Filtre tous les visuels de la page et rafraîchit les analyses

### Fonctionnalités
- Navigation intuitive par boutons pays
- Comparaison des performances par catégorie
- Analyse temporelle pour identifier les tendances
- Drill-through possible pour détails par produit

---

## 🌈 Thème & Design

### Couleurs
- **Palette primaire :** Bleu, Orange, Gris
- **Fond :** Gris foncé (dark mode)
- **Texte :** Blanc ou gris clair
- **Accents :** Orange pour les données importante

### Polices
- **Titres :** Segoe UI Bold, 16-20pt
- **Texte :** Segoe UI Regular, 11-14pt
- **Labels :** Segoe UI, 10-12pt

### Mise en page
- **Format :** 16:9 (Full HD)
- **Marge :** 20px sur tous les côtés
- **Espacement :** 10-15px entre visuels
- **Alignement :** Grille 3x3 pour meilleure lisibilité

---

## 📄 Fichiers d'images

### page_overview.png
- Capture d'écran de la Page 1
- Démonstration de la vue d'ensemble
- Format : PNG 1920x1080px

### page_pays.png
- Capture d'écran de la Page 2 avec Button Slicer
- Exemple avec filtrage par pays (ex: France)
- Format : PNG 1920x1080px

---

## 📄 Format des Screenshots

- **Résolution :** 1920 x 1080 pixels (Full HD)
- **Format :** PNG (sans perte)
- **Compression :** Optimisée pour web
- **Annotations :** Minimales (numéros de visuels si nécessaire)

---

*Dernière mise à jour : Mars 2026*
