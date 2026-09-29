# DevSupAi Site-Craft Methodology

> **La méthode d'ingénierie et d'orchestration pour concevoir un vrai site web professionnel avec l'intelligence artificielle, étape par étape.**

Ce dépôt contient le framework méthodologique et le **Skill interactif** officiel développé par [DevSupAi](https://www.devsupai.fr), conçu pour transformer un agent IA (Antigravity, Claude Code, Cursor, Codex) en un **Directeur de Projet Web chevronné**.

Il permet de quitter le « vibe coding » désordonné et les résultats génériques pour appliquer une démarche d'ingénierie web rigoureuse : cadrage stratégique, design system sur-mesure, formulation CROC, audits d'accessibilité et Quality Gates avant mise en ligne.

---

## Pourquoi cette méthode ?

L'intelligence artificielle sait taper du code à une vitesse fulgurante, mais **elle ne sait pas décider à votre place**. Livrée à elle-même, une IA a des automatismes : textes passe-partout sans ancrage local, dégradés violets criards, composants mal contrastés, failles de sécurité et oubli du mobile.

Cette méthode repose sur un principe fondateur :
* **Vous dirigez en maître d'ouvrage et architecte :** Vous définissez le besoin, arbitrez les choix visuels et testez sur de vrais terminaux.
* **L'IA exécute sous contrainte chirurgicale :** Elle assemble le code brique par brique selon vos règles et ne saute aucune étape de contrôle.

---

## Les 3 Piliers du Système

### 1. Les 3 Documents de Référence
Dès le début du chantier, le skill génère trois artefacts clés à la racine du projet :
* **`PROJET.md` :** La boussole métier (les 6 questions de cadrage, l'objectif unique, la cible, la concurrence, l'arborescence « une page = une intention »).
* **`DESIGN.md` :** Les tokens immuables (palette contrastée ratio >= 4.5:1, typographies, échelle d'espacement 4-64px, zéro emoji, mobile-first).
* **`AGENTS.md` :** Le règlement intérieur du chantier (périmètre chirurgical, zéro dépendance sauvage, étanchéité des secrets, validation Git).

### 2. La Méthode CROC pour Piloter l'Agent
Chaque consigne de développement est formulée selon l'acronyme CROC :
* **C (Contexte) :** Où en est le projet et quels fichiers consulter.
* **R (Résultat attendu) :** Le comportement et l'apparence exacte sans ambiguïté.
* **O (Ontraintes / Contraintes) :** Ce qu'il ne faut pas modifier, règles de sécurité et d'accessibilité.
* **C (Contrôle) :** La commande de vérification locale (build, responsive 375px/1440px) et le résumé exigé.

### 3. Les Quality Gates avant Déploiement
Aucun site n'est mis en ligne sans validation de la matrice de conformité :
1. *Gate 1 : Cadrage & Contenu* (zéro donnée inventée, textes authentiques).
2. *Gate 2 : Design & Ergonomie* (contrastes WCAG AA, boutons tactiles >= 44px).
3. *Gate 3 : SEO Technique* (H1 séquentiel, sitemap.xml, robots.txt, Schema.org JSON-LD).
4. *Gate 4 : Performance & CWV* (formats WebP/AVIF, dimensions explicites, bundle maîtrisé).
5. *Gate 5 : Sécurité & Légal* (zéro secret client, formulaires protégés, mentions légales, RGPD).

---

## Le Cycle de Vie en 12 Étapes

1. **Cadrage métier** (Les 6 questions fondamentales et formalisation de `PROJET.md`).
2. **Contenu & Référencement** (Mots-clés locaux, une intention par page, FAQ réelle).
3. **Direction artistique & Mockups** (Inspirations, palette contrastée, directives anti-clichés IA, validation sur maquette/mockup, formalisation de `DESIGN.md`).
4. **Stack & Règles** (Choix technique adapté, `AGENTS.md` et initialisation Git).
5. **Construction par étapes CROC** (Fondations, en-tête, accueil section par section, pages secondaires).
6. **Fonctionnalités sensibles** (Formulaires avec honeypot, base sécurisée J1, Stripe Checkout).
7. **Animations mesurées** (Transitions courtes 150-400ms, respect de `prefers-reduced-motion`).
8. **SEO & AEO technique** (Balisage sémantique, métadonnées, Schema.org, test code source brut).
9. **Piliers qualité** (Vitesse Core Web Vitals, navigation clavier, tests sur vrais smartphones).
10. **Cadre juridique** (Mentions légales, politique de confidentialité, consentement cookies).
11. **Mise en ligne méthodique** (Checklist de release et verdict Quality Gates).
12. **Pilotage post-lancement** (Suivi semaine 1 et optimisation Search Console à 3 mois).

---

## Installation & Utilisation

### Option 1 : Utilisation avec Google Antigravity

Pour installer ce skill de manière globale dans votre environnement Antigravity :

```bash
# Cloner le dépôt dans votre dossier de skills globaux
git clone https://github.com/devsupai/site-craft-methodology.git ~/.gemini/config/skills/site-craft-methodology
```

Une fois installé, lancez simplement sur un nouveau projet :
> « Active le skill site-craft-methodology et aide-moi à cadrer un nouveau site web. »

L'agent endosse immédiatement le rôle de directeur de projet et démarre l'interrogatoire guidé de l'étape 1.

### Option 2 : Utilisation avec Claude Code, Cursor ou Codex

Copiez le contenu de `SKILL.md` dans vos instructions de projet ou dans votre fichier de règles local (`CLAUDE.md`, `.cursorrules` ou `AGENTS.md`), et utilisez les fichiers du dossier `templates/` pour initialiser votre espace de travail.

---

## Contenu du Dépôt

```text
├── README.md                 # Documentation complète et guide d'utilisation
├── LICENSE                   # Licence open-source MIT
├── SKILL.md                  # Cœur du skill IA (machine d'états, protocoles, consignes CROC)
├── templates/
│   ├── PROJET.template.md    # Template de cadrage stratégique et personas
│   ├── DESIGN.template.md    # Template de design system et tokens CSS
│   ├── AGENTS.template.md    # Template du règlement intérieur du chantier
│   └── quality-gates.template.md # Grille d'évaluation des preuves tangibles
└── examples/
    └── artisan-electricien/  # Exemple complet d'un projet mené avec la méthode
        ├── PROJET.md
        ├── DESIGN.md
        └── AGENTS.md
```

---

## Licence

Ce projet est sous licence [MIT](LICENSE). Vous êtes libre de l'utiliser, le modifier et l'intégrer dans vos projets personnels et commerciaux.
