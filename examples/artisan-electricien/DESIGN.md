# Design System : Électricité Meuse Dépannage

Tokens graphiques et règles visuelles pour le site vitrine local.

---

## 1. Directives Graphiques

* **Mobile-First :** Ergonomie pensée pour un pouce en situation d'urgence (bouton d'appel flottant en bas de l'écran sur mobile).
* **Zéro Emoji :** Icônes techniques SVG Lucide (Zap, ShieldCheck, Clock, MapPin, PhoneCall).
* **Sobriété :** Palette inspirée de l'énergie et de la sécurité (bleu sécurité, orange avertissement discret, fond blanc cassé).

---

## 2. Tokens Chromatiques

```css
:root {
  --color-primary: #0284C7;        /* Bleu intervention rassurant */
  --color-primary-hover: #0369A1;
  --color-secondary: #0F172A;      /* Fond sombre et titres */
  --color-accent: #F59E0B;         /* Touche d'alerte / urgence modérée */

  --color-bg-base: #FFFFFF;
  --color-bg-subtle: #F8FAFC;
  --color-bg-elevated: #FFFFFF;

  --color-text-main: #0F172A;      /* Contraste 13.5:1 sur blanc */
  --color-text-muted: #475569;     /* Contraste 5.2:1 sur blanc */

  --color-border: #E2E8F0;
}
```

---

## 3. Typographie

* **Titres :** `Montserrat`, sans-serif (graisse 800 pour inspirer robustesse et sécurité).
* **Corps :** `Plus Jakarta Sans`, sans-serif (graisse 400 et 600, lisibilité immédiate).
* **Bouton d'urgence :** Texte en gras `16px`, zone cliquable `52px` de hauteur.
