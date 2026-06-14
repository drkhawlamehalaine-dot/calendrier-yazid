# Agenda Présidentiel — Guide

Deux fichiers, deux rôles :

- **`index.html`** → la page que le président ouvre (lecture seule, toujours à jour).
- **`evenements.json`** → le fichier que **toi** tu modifies pour ajouter/changer les réunions.

---

## Mise en place (une seule fois)

1. Crée un dépôt GitHub (ex : `agenda-president`).
2. Mets-y les deux fichiers : `index.html` et `evenements.json`.
3. Va dans **Settings → Pages**.
4. Sous "Source", choisis la branche `main` et le dossier `/ (root)`. Enregistre.
5. Au bout d'une minute, GitHub te donne un lien du type :
   `https://ton-nom.github.io/agenda-president/`
6. Envoie **ce lien** au président. C'est tout ce dont il a besoin.

---

## Ajouter une réunion (toi, à chaque fois)

1. Ouvre `evenements.json` sur GitHub → clique sur le crayon ✏️ pour éditer.
2. Ajoute un bloc sous la date voulue. Format de la date : `AAAA-MM-JJ`.

```json
"2026-07-03": [
  {
    "titre": "Sommet économique",
    "heure": "14:00",
    "type": "Diplomatique",
    "note": "Lieu et participants ici"
  }
]
```

3. Types possibles : `Officiel`, `Confidentiel`, `Diplomatique`, `Interne`.
4. Clique **Commit changes**.
5. Le président rafraîchit sa page → la réunion apparaît. (La page se resynchronise aussi seule toutes les 2 minutes.)

> Astuce : plusieurs réunions le même jour = plusieurs blocs `{ }` séparés par une virgule à l'intérieur des crochets `[ ]`.

---

## Attention au format JSON

- Chaque accolade `{` doit être fermée par `}`.
- Une virgule entre deux éléments, **jamais** après le dernier.
- Si la page affiche "Hors ligne", c'est presque toujours une virgule en trop ou un guillemet manquant. Colle ton fichier dans https://jsonlint.com pour vérifier.
