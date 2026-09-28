# Design System & Spécifications Visuelles : [Nom du Projet]

Document de référence fixant les tokens et directives graphiques selon la méthode Site-Craft DevSupAi.
Une fois ce document validé, l'agent d'IA a l'interdiction stricte d'improviser des couleurs, des espacements ou des typographies arbitraires.

---

## 1. Principes Fondamentaux de Conception

1. **Mobile-First Impératif :** Tout composant est conçu et validé en premier lieu pour une largeur de 375px avant d'être adapté aux grands écrans.
2. **La Règle des 3 Secondes :** Le visiteur doit comprendre en moins de 3 secondes qui parle, quelle est la proposition de valeur, et où cliquer.
3. **Un Seul Appel à l'Action Principal par Écran :** Pas de dispersion d'attention.
4. **Le Pouvoir du Vide :** Des marges généreuses pour laisser respirer l'œil et hiérarchiser l'information.
5. **Zéro Emoji :** Bannissement total des symboles emoji dans le code et les interfaces. Utilisation exclusive d'icônes vectorielles SVG soignées (ex: Lucide Icons).
6. **Ergonomie Tactile :** Boutons et liens d'au moins 44x44px de zone de frappe, taille de texte courante minimale de 16px.

---

## 2. Palette Chromatique & Tokens de Couleur

Tous les couples texte/fond doivent respecter un ratio de contraste supérieur ou égal à **4.5:1** (norme WCAG AA).

```css
:root {
  /* Nuances Principales */
  --color-primary: #0284C7;        /* Couleur de marque / CTA principal */
  --color-primary-hover: #0369A1;  /* État au survol */
  --color-secondary: #0F172A;      /* Couleur de structure / Titres */
  --color-accent: #38BDF8;         /* Touches d'accentuation subtiles */

  /* Surfaces & Fonds */
  --color-bg-base: #FFFFFF;        /* Fond de page principal */
  --color-bg-subtle: #F8FAFC;      /* Fond de section alternatif */
  --color-bg-elevated: #FFFFFF;    /* Fond de carte ou dialogue */

  /* Textes */
  --color-text-main: #1E293B;      /* Texte courant (contraste élevé) */
  --color-text-muted: #475569;     /* Texte secondaire, labels */
  --color-text-light: #94A3B8;     /* Mentions discrètes */

  /* Bordures & Séparateurs */
  --color-border: #E2E8F0;         /* Bordures standards */
  --color-border-subtle: #F1F5F9;  /* Séparateurs légers */

  /* États Système */
  --color-success: #16A34A;
  --color-warning: #D97706;
  --color-danger: #DC2626;
}
```

---

## 3. Typographie & Hiérarchie de Texte

* **Police Titres (Headings) :** `Montserrat`, sans-serif (caractère affirmé, graisses 700 et 900).
* **Police Corps (Body) :** `Plus Jakarta Sans`, sans-serif (lisibilité optimale sur mobile, graisses 400 et 600).
* **Échelle Typographique :**
  * `H1` : `clamp(2rem, 5vw, 3.25rem)` / Interligne : 1.15 / Graisse : 900
  * `H2` : `clamp(1.5rem, 3.5vw, 2.25rem)` / Interligne : 1.25 / Graisse : 800
  * `H3` : `1.25rem` / Interligne : 1.35 / Graisse : 700
  * `Corps (P)` : `1rem (16px)` à `1.125rem (18px)` / Interligne : 1.6 / Graisse : 400
  * `Petit texte (Mentions)` : `0.875rem (14px)` / Interligne : 1.5 / Graisse : 500

---

## 4. Grille Mathématique des Espacements

Interdiction formelle d'insérer des marges aléatoires (ex: `13px`, `27px`).
Utiliser exclusivement l'échelle mathématique :

* `space-1` : `4px`
* `space-2` : `8px`
* `space-3` : `12px`
* `space-4` : `16px`
* `space-6` : `24px`
* `space-8` : `32px`
* `space-12` : `48px`
* `space-16` : `64px`
* `space-24` : `96px`

---

## 5. Composants Clés & États d'Interaction

### Bouton Principal (CTA)
* Hauteur minimale : `44px`
* Rembourrage (padding) : `12px 24px`
* Rayon de bordure : `10px` à `12px` (coins légèrement adoucis, sans pilule excessive)
* États obligatoires :
  * *Repos :* Fond `--color-primary`, texte blanc.
  * *Survol (Hover) :* Fond `--color-primary-hover`, translation légère `-1px`.
  * *Focus clavier :* Anneau de focus visible `outline: 2px solid --color-primary; outline-offset: 2px`.
  * *Actif / Clic :* Léger enfoncement `scale(0.98)`.
  * *Désactivé :* Opacité 0.5, curseur `not-allowed`.

### Cartes (Cards)
* Fond : `--color-bg-elevated`
* Bordure : `1px solid --color-border`
* Ombre : Ombre douce et diffuse (bannir les ombres lourdes opaques)
* Rembourrage : `24px` sur mobile, `32px` sur écran large.

### Champs de Formulaire
* Hauteur : `44px` minimum.
* Bordure : `1px solid --color-border`, devient `--color-primary` avec anneau de focus à la prise de sélection.
* Label toujours visible au-dessus du champ (pas de placeholder servant d'unique étiquette).

---

## 6. Comportement du Mouvement & Animations

* **Durées d'animation :** Entre `150ms` et `350ms` au maximum.
* **Courbe d'accélération :** `cubic-bezier(0.16, 1, 0.3, 1)` pour des mouvements naturels.
* **Accessibilité Mouvement :**
  ```css
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
  }
  ```
* **Règle de l'effet signature :** Un seul effet remarquable au défilement par page. Tout le reste est sobre et fonctionnel.
