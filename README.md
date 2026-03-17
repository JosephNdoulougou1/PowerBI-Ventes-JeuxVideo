# 📊 PowerBI - Analyse des Ventes de Jeux Vidéo

> **Dashboard interactif Power BI** | Analyse des ventes vidéo jeux 2021-2023 | **13,1M€** de chiffre d'affaires | Modèle en étoile | DAX avancé | 9 marchés couverts

---

## 📂 Structure du Projet

```
📁 PowerBI-Ventes-JeuxVideo/
├── 📊 Rapport_Ventes.pbix          # Fichier Power BI principal
├── 📁 data/
│   └── Extraction_des_Ventes.xlsx  # Source : 3 tables (Ventes, Produits, Clients)
├── 📁 screenshots/
│   ├── page_overview.png
│   └── page_pays.png
└── 📄 README.md
```

---

## 🗃️ Source de Données

Fichier Excel avec **3 tables interconnectées** :

| Table | Lignes | Colonnes clés |
|-------|--------|---------------|
| **Ventes** | 13 899 | Date commande, Quantité, Prix unitaire, Coût unitaire, Pays |
| **Liste des Produits** | 2 517 | Nom, Marque, Catégorie, Sous-catégorie, Prix, Coût |
| **Liste des Clients** | 5 585 | Prénom, Nom, Ville, État, Pays, Code pays |

**🌍 Couverture géographique :** Allemagne · Australie · Canada · États-Unis · France · Italie · Pays-Bas · Royaume-Uni · En ligne

**📅 Période :** Janvier 2021 → Octobre 2023

---

## 📐 Modèle de Données (Star Schema)

```
Ventes ──── [Clé Produit] ────► Liste des Produits
Ventes ──── [Clé Client] ─────► Liste des Clients
```

✅ **Relations Many-to-One**  
✅ **Filtre directionnel unique**  
✅ **Modèle optimisé pour performances DAX**

---

## 📈 KPIs & Mesures DAX

### Mesures Principales

```dax
-- Chiffre d'affaires total
CA Total = SUMX(Ventes, Ventes[Quantité] * Ventes[Prix Unitaire])

-- Coût total
Coût Total = SUMX(Ventes, Ventes[Quantité] * Ventes[Coût Unitaire])

-- Marge brute
Marge Brute = [CA Total] - [Coût Total]

-- Taux de marge (%)
Taux de Marge % = DIVIDE([Marge Brute], [CA Total], 0) * 100

-- Évolution année sur année (%)
CA YoY % = 
VAR CA_N = [CA Total]
VAR CA_N1 = CALCULATE([CA Total], SAMEPERIODLASTYEAR('Calendrier'[Date]))
RETURN DIVIDE(CA_N - CA_N1, CA_N1, 0) * 100
```

### Chiffres Clés (Toutes Périodes)

| KPI | Valeur |
|-----|--------|
| 💰 **CA Total** | **13,1 M€** |
| 🏭 **Coût Total** | **5,4 M€** |
| 📊 **Marge Brute** | **7,7 M€** |
| 📦 **Nb Transactions** | **13 899** |
| 🌍 **Marchés Couverts** | **9** |
| 🛒 **Produits Référencés** | **2 517** |
| 👥 **Clients** | **5 585** |

---

## 🖥️ Pages du Rapport

### 📍 **Page 1 — Vue d'Ensemble (Overview)**

- **Cards :** Coût total · CA · Marge Brute
- **Carte Bing :** Distribution géographique des ventes
- **Slicer :** Filtrage par Point de vente (pays + en ligne)

### 📍 **Page 2 — Analyse par Catégorie & Année**

- **Bar Chart :** CA par Catégorie (Audio, Culture, Électroménagers, Jeux, Ordinateurs, Photo, Smartphones, Vidéo)
- **Bar Chart Horizontal :** CA par Année (2021 vs 2022 vs 2023)
- **Donut Chart :** Répartition CA par Catégorie
- **Button Slicer :** Navigation par pays (style tableau de bord professionnel)

---

## 🔧 Outils & Technologies

| Outil | Usage |
|-------|-------|
| **Power BI Desktop** | Modélisation, DAX, visuels, mise en page |
| **Power Query (M)** | Nettoyage, typage, jointures |
| **Microsoft Excel** | Source de données (.xlsx, 3 feuilles) |
| **DAX** | Mesures calculées, time intelligence |
| **JSON** | Thème personnalisé (design sombre) |

---

## 🚀 Comment Utiliser ce Projet

### 1️⃣ Cloner le Dépôt

```bash
git clone https://github.com/JosephNdoulougou1/PowerBI-Ventes-JeuxVideo.git
```

### 2️⃣ Ouvrir le Rapport

- Ouvrir `Rapport_Ventes.pbix` avec **Power BI Desktop** (version ≥ Mars 2024)

### 3️⃣ Relier la Source de Données

- Transformer les données → Modifier les paramètres
- Changer le chemin vers : `data/Extraction_des_Ventes.xlsx`

### 4️⃣ Actualiser

- Cliquer sur **Actualiser** → Les visuels se mettent à jour automatiquement

---

## 💡 Points Techniques Notables

✨ **Button Slicer personnalisé** pour navigation par pays (style tableau de bord professionnel)  
✨ **Time Intelligence** avec table Calendrier marquée pour comparaisons YoY  
✨ **Thème sombre appliqué** via fichier JSON pour rendu homogène  
✨ **Star Schema optimisé** pour performances DAX  
✨ **Drill-through possible** par pays et par catégorie

---

## 📚 Compétences Démontrées

⚙️ Modélisation en étoile et gestion des relations dans Power BI  
🧮 Mesures DAX avancées (CALCULATE, DIVIDE, SUMX, SAMEPERIODLASTYEAR)  
🔄 Nettoyage et transformation des données avec Power Query (M)  
🎨 Design UI/UX d'un rapport professionnel (thème sombre, navigation, cohérence visuelle)  
📉 Analyse financière : CA, marge brute, évolution YoY, segmentation géographique

---

## 👤 Auteur

**Joseph Ndoulougou**  
📧 josephmorel20@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/josephndoulougou)  
💼 Étudiant(e) en Master Data / Finance — En recherche d'alternance

---

## 📄 Licence

Ce projet est réalisé dans le cadre d'un **portfolio personnel**.  
Les données sont **fictives** et utilisées à des fins pédagogiques uniquement.

---

*Dernière mise à jour : Mars 2026*
