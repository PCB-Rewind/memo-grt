# 🗒️ Mémo GRT

Appli web de mémo partagé pour suivre **toutes les tâches à faire**, au fil de l'eau, sur tous tes appareils.
Ajoute une tâche, coche-la (elle passe en barré), et vide les tâches faites en fin de semaine. Une seule liste, synchronisée entre Mac, iPhone et Android.

**→ [Ouvrir l'appli](https://TON-PSEUDO.github.io/memo-grt/)**

---

## Ce que ça fait

- **Ajout au fil de l'eau** : une tâche, Entrée, elle s'empile en haut de la liste.
- **Coche en barré** : tu marques une tâche faite, elle reste visible mais barrée et grisée, jamais perdue de vue.
- **Casquettes** (optionnel) : colle une étiquette CMO, CFO, CTO, COO ou CEO à une tâche, qui colore la barre de gauche selon la casquette.
- **Filtres** : toutes, à faire, ou faites, en un clic.
- **Vider en fin de semaine** : un bouton (double clic pour confirmer) nettoie toutes les tâches faites d'un coup.
- **Cache local** : la liste s'affiche instantanément et reste lisible même hors ligne, puis se resynchronise dès que le réseau revient.
- Fonctionne sur **Mac, iPhone, Android**, une seule URL, tâches synchronisées.

---

## Premier lancement

À l'ouverture, le portail demande deux choses :

| Champ | Quoi |
|---|---|
| **Bin ID** | L'identifiant du seau qui stocke tes tâches (voir ci-dessous). |
| **Master Key** | La clé d'accès au seau. |

Tout est mémorisé sur l'appareil : tu ne le tapes qu'une fois. Le bouton « changer » en haut à droite rouvre le portail si besoin.

### Créer le seau (2 min, gratuit, sans carte bancaire)

1. Va sur [jsonbin.io](https://jsonbin.io) et crée un compte gratuit.
2. **Create Bin**, colle `{"tasks":[]}` comme contenu, sauve. Le **Bin ID** est dans l'URL.
3. Menu **API Keys**, copie ta **Master Key** (commence par `$2a$`).
4. Utilise le même Bin ID et la même Master Key sur chacun de tes appareils pour retrouver la même liste partout.

> ⚠️ Crée un seau dédié au mémo, différent de celui du running Motocultor : les deux applis stockent des données de forme différente et ne doivent pas partager le même seau.

> ⚠️ La Master Key donne accès en écriture au seau. À garder pour toi, jamais en public.

---

## Mettre à jour l'appli

L'appli est un seul fichier : `index.html`.
Pour publier une nouvelle version, remplace `index.html` dans ce dépôt, GitHub Pages republie tout seul en une minute environ. L'URL ne change pas.

---

## Technique

- HTML / CSS / JS purs, **aucune dépendance**, un seul fichier.
- Stockage des tâches via [JSONBin.io](https://jsonbin.io) (seau JSON), en-tête `X-Master-Key`.
- Hébergé sur **GitHub Pages**.
- Thème clair chaleureux, accessible, responsive, `prefers-reduced-motion` respecté.

---

*Même forme de connexion que l'appli Running Motocultor : un portail Bin ID + Master Key, stocké en local sur chaque appareil.*
