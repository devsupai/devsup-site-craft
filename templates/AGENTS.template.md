# Règlement Intérieur du Chantier : Directives pour Agents IA

Ce document constitue le règlement intérieur imposé à tout agent d'IA intervenant sur ce dépôt de code (Antigravity, Claude Code, Cursor, Codex).
Toute intervention qui déroge à ces règles sera immédiatement annulée par l'opérateur humain.

---

## 1. Respect des Documents Piliers

* **Boussole métier :** L'agent doit impérativement lire et respecter les objectifs consignés dans `PROJET.md`.
* **Tokens immuables :** L'agent puise exclusivement dans les couleurs, espacements et polices définis dans `DESIGN.md`. Il lui est interdit d'inventer des classes arbitraires ou des nuances personnalisées.

---

## 2. Règle du Périmètre Chirurgical

* **Non-dispersion :** L'agent ne modifie que les fichiers strictement mentionnés dans la consigne en cours.
* **Préservation de l'existant :** Ne jamais reformater, supprimer ou réécrire un composant sans consigne explicite.
* **Gestion des effets secondaires :** Toute modification de configuration (`package.json`, `tailwind.config`, `tsconfig`) exige une validation préalable de l'utilisateur.

---

## 3. Maîtrise des Dépendances & Sécurité

* **Zéro installation sauvage :** Interdiction absolue de lancer `npm install` ou d'ajouter une bibliothèque externe sans accord explicite de l'utilisateur.
* **Étanchéité des secrets :** Aucun token d'administration, identifiant sensible ou clé d'API privée ne doit figurer dans le code client ou être commité dans le dépôt Git.
* **Validation des formulaires :** Tout formulaire doit comporter une validation des données saisies (côté client et serveur), une protection anti-spam invisible (honeypot) et une mention RGPD.

---

## 4. Rigueur Visuelle & Accessibilité (A11y)

* **Approche Mobile-First :** Tout composant doit être conçu pour fonctionner parfaitement à 375px de large avant grand écran.
* **Zéro Emoji :** Interdiction absolue d'insérer des symboles emoji dans le code ou l'interface. Utiliser exclusivement des icônes vectorielles SVG.
* **Bannissement du tiret cadratin :** Ne jamais insérer le caractère tiret cadratin (`—`, Unicode U+2014) ; utiliser exclusivement le tiret standard (`-`).
* **Navigation clavier :** Tout élément interactif (bouton, lien, modale) doit être utilisable au clavier avec un anneau de focus visible.
* **Sémantique :** Exactement un seul `<h1>` par page, suivi d'une arborescence séquentielle sans saut (`<h1>` -> `<h2>` -> `<h3>`).

---

## 5. Protocole de Fin de Tâche

Après chaque intervention, l'agent d'exécution doit obligatoirement :

1. Lancer la commande de vérification locale (ex: `npm run build` ou `npx tsc --noEmit`).
2. S'assurer qu'aucune erreur ou avertissement bloquant ne subsiste.
3. Résumer factuellement à l'utilisateur :
   * Les fichiers modifiés.
   * Le résultat obtenu.
   * La commande de test exécutée.
   * Inviter l'utilisateur à vérifier le rendu dans son navigateur avant de valider le commit Git.
