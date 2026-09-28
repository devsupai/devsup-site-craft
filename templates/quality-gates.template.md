# Grille d'Évaluation des Quality Gates & Contrôle de Release

Document de contrôle final à remplir impérativement avant toute validation de mise en ligne.
Aucune mise en production ne peut être prononcée sans un verdict global `PASS`.

---

## 1. Matrice des Quality Gates

Chaque porte de qualité doit être validée par une preuve tangible mesurée ou vérifiée localement.

| Porte de qualité (Gate) | Statut exigé | Preuve tangible mesurée ou constatée | Verdict |
| :--- | :--- | :--- | :--- |
| **Gate 1 : Cadrage & Contenu** | PASS | `PROJET.md` validé, zéro fausse statistique, zéro texte générique, vraies anecdotes et coordonnées locales vérifiées | [ ] PASS [ ] FAIL |
| **Gate 2 : Design & Ergonomie** | PASS | Tokens `DESIGN.md` respectés, contrastes texte/fond >= 4.5:1, zones tactiles >= 44px, zéro emoji, responsive 375px et 1440px | [ ] PASS [ ] FAIL |
| **Gate 3 : SEO & AEO Technique** | PASS | Exactement un `<h1>` par page, balises Title/Meta uniques, sitemap.xml, robots.txt, schémas Schema.org JSON-LD valides, texte présent dans le HTML source brut | [ ] PASS [ ] FAIL |
| **Gate 4 : Performance & CWV** | PASS | Compilation locale propre, bundle JS/CSS maîtrisé, images converties en WebP/AVIF avec dimensions explicites (width/height), chargement différé des scripts non critiques | [ ] PASS [ ] FAIL |
| **Gate 5 : Sécurité & Légal** | PASS | Zéro clé API ou secret dans le code client, formulaires avec honeypot et validation, mentions légales complètes, politique de confidentialité RGPD, bandeau cookies conforme | [ ] PASS [ ] FAIL |

---

## 2. Checklist d'Avant-Lancement (7 Points Critiques)

* [ ] **1. Compilation locale sans erreur :** La commande de build s'exécute à 100% avec succès sans avertissement bloquant (`npm run build`).
* [ ] **2. Étanchéité des variables d'environnement :** Toutes les clés de production sont renseignées sur la plateforme d'hébergement, aucune clé dans le code source.
* [ ] **3. Nom de domaine & HTTPS :** Enregistrements DNS configurés, certificat SSL actif (cadenas vert).
* [ ] **4. Redirections permanentes (si refonte) :** Redirections 301 mises en place pour les anciennes adresses URL afin de préserver le référencement existant.
* [ ] **5. Indexation & Mesure :** Fichier `sitemap.xml` soumis dans Google Search Console, balise de mesure d'audience anonymisée active.
* [ ] **6. Test physique complet en conditions réelles :** Parcours utilisateur exécuté sur un smartphone iPhone et un smartphone Android (envoi réel d'un formulaire de contact).
* [ ] **7. Tag de version Git :** Commit de release étiqueté dans Git (`git tag -a v1.0.0 -m "Release v1.0.0"`).

---

## 3. Règle Épistémique pour les Rapports d'Audit

* `MESURÉ` : Mesure instrumentée réellement effectuée localement (ex: poids du bundle JS = 84 kB gzip).
* `NON MESURÉ` : Mesure impossible en local ou nécessitant des données réelles d'utilisateurs (ex: Core Web Vitals en conditions réelles RUM).
* `ESTIMÉ` : Calcul projectif explicitement identifié comme tel.
* `QUALITATIF` : Constat issu de la revue de code (ex: présence d'un attribut alt informatif).
