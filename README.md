# 🇹🇭 Aromea – Site Web du restaurant thaïlandais

Ce projet est un **site vitrine complet** pour **Aromea**, un restaurant thaïlandais fictif, réalisé dans le cadre d’un **projet de BTS SIO**.

---

## 🧾 Fonctionnalités principales

- ✅ Page d’accueil avec **bannière**, **présentation du restaurant** et **plats populaires**
- 🧭 Affichage dynamique du **header** et du **footer** sur toutes les pages
- 🍜 **Menu complet** avec plats, desserts et boissons en grille
- 🛒 Page **commande** avec :
  - panier interactif (localStorage)
  - total en temps réel
  - badge dynamique dans la navigation
  - formulaire client
  - enregistrement des commandes dans Firebase 🔥
- 📍 Page contact avec **formulaire de contact** et **carte Google Maps**
- 📱 Design responsive moderne (mobile, tablette, ordinateur)

---

## 🛠️ Technologies utilisées

- `HTML5` – Structure du site  
- `CSS3` – Mise en page et design  
- `JavaScript` – Interaction utilisateur (panier, badge, formulaires…)  
- `Firebase` – Enregistrement des commandes (Firestore)  
- `Visual Studio Code` – Éditeur utilisé  
- `Git / GitHub` – Suivi de version et publication  

---

## 🔥 Intégration Firebase

Le site utilise [**Firebase Firestore**](https://firebase.google.com/) pour **sauvegarder les commandes clients**.

- Connexion sécurisée (clé API côté client)
- Base Firestore en mode **test sécurisé (lecture/écriture)**
- Chaque commande comprend : nom, téléphone, adresse, articles, total, et date

---

## 📁 Arborescence du projet

```
/images              → images du site (plats, fond, logo…)
index.html           → page d’accueil
menu.html            → page du menu
commande.html        → page de commande avec panier
contact.html         → page de contact
header.html          → en-tête réutilisable
footer.html          → pied de page réutilisable
style.css            → feuille de style principale
```

---

## 🗺️ Adresse du restaurant

**8 Avenue des Chartreux, Marseille, France**  
Carte intégrée dans `index.html` via **Google Maps Embed**.

---

## 🚀 Déploiement

> Le site pourra être mis en ligne via **GitHub Pages** ou hébergement Firebase.


## 👤 Auteur

Projet réalisé par **Iliassedzz**  
🎓 Année scolaire : **2025**  
📁 Projet présenté dans le cadre du **BTS SIO**
