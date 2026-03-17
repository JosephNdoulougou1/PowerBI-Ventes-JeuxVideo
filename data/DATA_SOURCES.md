# 🗃️ Sources de Données

## Vue d'ensemble

Le projet PowerBI utilise **3 tables interconnectées** stockées dans un fichier Excel :

**Fichier source :** `Extraction_des_Ventes.xlsx`

---

## 📋 Tables de Données

### 1. Table **Ventes** (13,899 lignes)

| Colonne | Type | Description |
|---------|------|-------------|
| `Clé Vente` | Numérique | Identifiant unique de la transaction |
| `Date Commande` | Date | Date de la commande (YYYY-MM-DD) |
| `Clé Client` | Numérique | Référence vers la table Clients |
| `Clé Produit` | Numérique | Référence vers la table Produits |
| `Quantité` | Numérique | Nombre d'unités vendues |
| `Prix Unitaire` | Décimal | Prix de vente HT par unité |
| `Coüt Unitaire` | Décimal | Coût d'achat par unité |
| `Pays` | Texte | Pays de livraison |

**Période couverte :** Janvier 2021 → Octobre 2023

---

### 2. Table **Liste des Produits** (2,517 lignes)

| Colonne | Type | Description |
|---------|------|-------------|
| `Clé Produit` | Numérique | Identifiant unique du produit |
| `Nom Produit` | Texte | Nom commercial du produit |
| `Marque` | Texte | Marque du fabricant |
| `Catégorie` | Texte | Catégorie principale (Audio, Jeux, etc.) |
| `Sous-Catégorie` | Texte | Sous-classification du produit |
| `Prix Vente` | Décimal | Prix de vente standard |
| `Coût` | Décimal | Coût d'achat |
| `Poids` | Décimal | Poids en kg (pour logistique) |

**Catégories disponéures :**
- Audio
- Culture
- Électroménagers
- Jeux
- Ordinateurs
- Photo
- Smartphones
- Vidéo

---

### 3. Table **Liste des Clients** (5,585 lignes)

| Colonne | Type | Description |
|---------|------|-------------|
| `Clé Client` | Numérique | Identifiant unique du client |
| `Prénom` | Texte | Prénom du client |
| `Nom` | Texte | Nom de famille |
| `Ville` | Texte | Ville de résidence |
| `État/Province` | Texte | État ou province |
| `Code Pays` | Texte | Code pays ISO (DE, AU, CA, etc.) |
| `Pays` | Texte | Nom complet du pays |
| `Email` | Texte | Adresse e-mail (si disponible) |
| `Date Inscription` | Date | Date d'ajout au système |

---

## 🌍 Couverture Géographique

✓ Allemagne (DE)  
✓ Australie (AU)  
✓ Canada (CA)  
✓ États-Unis (US)  
✓ France (FR)  
✓ Italie (IT)  
✓ Pays-Bas (NL)  
✓ Royaume-Uni (GB)  
✓ En ligne (Online)  

---

## 🔗 Relations entre Tables

```
┌─────────────────────┐
│   Ventes            │
├─────────────────────┤
│ Clé Vente (PK)     │
│ Clé Client (FK)    ├───────────┐
│ Clé Produit (FK)   ├───────────┐
│ ...                 │           │
└─────────────────────┘           │
           │                      │
        (Many)                  (Many)
           │                      │
      (One)|                      |(One)
           │                      │
┌──────────────────────────┐  ┌──────────────────────┐
│  Liste des Clients       │  │ Liste des Produits   │
├──────────────────────────┤  ├──────────────────────┤
│ Clé Client (PK)         │  │ Clé Produit (PK)    │
│ Prénom, Nom, Pays...    │  │ Nom, Catégorie...   │
└──────────────────────────┘  └──────────────────────┘
```

**Type de relations :** Many-to-One  
**Direction de filtrage :** Unidirectionnelle

---

## 📂 Format et Encodage

- **Format fichier :** Microsoft Excel (.xlsx)
- **Encodage texte :** UTF-8
- **Séparateurs :** Virgule (',') pour les listes
- **Format dates :** YYYY-MM-DD
- **Format décimals :** Point ('.')

---

## 🔍 Qualité des Données

✓ **Pas de doublons** identifiés  
✓ **Clés primaires** uniques sur toutes les tables  
✓ **Références croisées** sans orphelins  
✓ **Dates valides** dans la plage spécifiée  
✓ **Montants** non négatifs sauf mentions spécifiques  

---

*Dernière validation : Mars 2026*
