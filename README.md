# 🥗 EatSmart - Application de Commande en Ligne

EatSmart est une application web moderne de prise de commandes pour un restaurant thaïlandais fictif. Le client peut consulter les plats, ajouter au panier, passer commande et voir le récapitulatif. Le projet s'appuie sur **Firebase Firestore** pour la base de données, **JavaScript moderne (ES6+)**, **CSS responsif** et une architecture en composants dynamiques via le `fetch()` du header/footer.

---

## 🚀 Fonctionnalités principales

- ✅ Affichage dynamique du menu depuis Firestore (`plats`, `desserts`, `boissons`)
- ✅ Ajout au panier avec animation et badge dynamique
- ✅ Système de panier persistant (stocké dans `localStorage`)
- ✅ Formulaire client avec validation HTML5
- ✅ Enregistrement des commandes dans Firestore
- ✅ Navigation vers une page de détails pour chaque plat
- ✅ Design moderne, responsive, avec animations et icônes FontAwesome
- ✅ Architecture modulaire avec `header.html`, `footer.html`, etc.

---

## 🗂 Structure du projet

```
eatsmart/
│
├── index.html              # Page d'accueil (présentation + bouton vers le menu)
├── menu.html               # Menu principal (plats, desserts, boissons)
├── commande.html           # Panier + formulaire client
├── details.html            # Détail d'un plat (chargé par ID)
│
├── header.html             # En-tête dynamique
├── footer.html             # Pied de page dynamique
│
├── style.css               # Feuille de styles globale
├── /images/                # Images des plats
├── /scripts/               # (optionnel) JS externes modulaires
│
└── README.md               # Ce fichier
```

---

## 🔧 Technologies utilisées

| Technologie        | Rôle                                      |
|--------------------|--------------------------------------------|
| **HTML5**          | Structure des pages                        |
| **CSS3**           | Design, responsive, animations modernes    |
| **JavaScript ES6+**| Logique (DOM, Firestore, panier, fetch...) |
| **Firebase Firestore** | Base de données cloud                |
| **Font Awesome**   | Icônes modernes (📞, 🏠, etc.)              |

---

## 🧠 Architecture et logique

### 🔹 Menu dynamique
- Récupération des plats depuis Firestore (`articles`)
- Affichage selon catégorie (`plats`, `desserts`, `boissons`)
- Chaque article contient un bouton "Ajouter au panier"

### 🔹 Panier local
- Stockage dans `localStorage` (`panierDetaille`)
- Calcul automatique du total
- Badge de panier dynamique dans le header

### 🔹 Commande client
- Formulaire avec validation (nom, adresse, téléphone)
- Les commandes sont envoyées vers Firestore (`commandes`)

### 🔹 Détail des plats
- Redirection vers `details.html?id=XXX`
- Affichage dynamique du plat sélectionné
- Ajout possible au panier depuis cette page

---

## 📦 Exemple de données Firebase

### 🔸 Collection `articles`

```json
{
  "nom": "Pad Thaï",
  "categorie": "plats",
  "prix": 9.90,
  "description": "Nouilles sautées aux légumes, cacahuètes et sauce thaï.",
  "images": "padthai.jpg"
}
```

### 🔸 Collection `commandes`

```json
{
  "nom": "Jean Dupont",
  "adresse": "12 rue des Lotus",
  "tel": "0612345678",
  "panier": [
    {
      "nom": "Pad Thaï",
      "quantite": 2,
      "prix": 9.90,
      "categorie": "plats"
    }
  ],
  "date": "2025-06-02T14:10:00.000Z"
}
```

---

## 🎨 Design et ergonomie

- Couleurs principales : orange `#f97316`, bleu `#1e293b`
- Icônes FontAwesome
- Effets de survol sur les boutons
- Design responsive pour mobile/tablette
- Layout centré avec `flex` + `grid`
- Message d’ajout au panier avec animation

---

## ✅ À faire / pistes d’amélioration

- [ ] Ajouter une interface admin pour voir les commandes
- [ ] Intégrer un système de paiement en ligne (ex : Stripe)
- [ ] Ajouter une gestion des stocks
- [ ] Intégrer un filtre par allergènes
- [ ] Mode sombre / clair

---

## 📚 Contexte pédagogique

Ce projet a été réalisé dans le cadre du **BTS SIO SLAM**, pour valider les compétences suivantes :

- 🔸 Consommation d'API Firebase
- 🔸 Stockage et lecture en NoSQL
- 🔸 Manipulation avancée du DOM
- 🔸 Gestion d’un panier e-commerce
- 🔸 Architecture modulaire frontend
- 🔸 Conception UI/UX moderne

---

## 🧩 Licence

Projet libre sous licence MIT  
Utilisation autorisée à des fins pédagogiques ou personnelles.

---

## 📸 Aperçus

![Aperçu menu](images/apercu-menu.png)  
![Aperçu détail](images/apercu-detail.png)
