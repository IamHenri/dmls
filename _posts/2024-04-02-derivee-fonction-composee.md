---
layout: post
title: "Exercice corrigé : dérivée d'une fonction composée (Terminale)"
date: 2024-04-02
category: Exercice corrigé
niveau: Terminale
readtime: 8
excerpt: "Un exercice complet sur le calcul de dérivée d'une fonction composée, avec la correction détaillée étape par étape. Idéal pour réviser avant le Bac."
---

Voici un exercice typique de Terminale sur la dérivation, avec une correction détaillée. C'est exactement le genre de question qui tombe au Bac.

## L'énoncé

Soit la fonction **f** définie sur ℝ par :

**f(x) = (3x² − 2x + 1)⁴**

1. Donner la forme de f sous forme d'une fonction composée g ∘ u.
2. Calculer f'(x).
3. Déterminer les valeurs de x pour lesquelles f'(x) = 0.

---

## Correction détaillée

### Question 1 — Identifier la composée

On pose :
- **u(x) = 3x² − 2x + 1** (la fonction intérieure)
- **g(t) = t⁴** (la fonction extérieure)

Ainsi, f(x) = g(u(x)) = (u(x))⁴ ✓

### Question 2 — Calculer f'(x)

On utilise la **règle de la chaîne** : (g ∘ u)' = u' × g'(u)

Calculs intermédiaires :
- u'(x) = 6x − 2
- g'(t) = 4t³, donc g'(u(x)) = 4·(3x² − 2x + 1)³

Application :

**f'(x) = (6x − 2) × 4(3x² − 2x + 1)³**

On peut factoriser :

**f'(x) = 4(6x − 2)(3x² − 2x + 1)³**

Ou encore : **f'(x) = 8(3x − 1)(3x² − 2x + 1)³**

### Question 3 — Annuler f'(x)

f'(x) = 0 ⟺ 8(3x − 1)(3x² − 2x + 1)³ = 0

**Cas 1 :** 3x − 1 = 0 → **x = 1/3**

**Cas 2 :** (3x² − 2x + 1)³ = 0 → 3x² − 2x + 1 = 0

Calcul du discriminant : Δ = 4 − 12 = **−8 < 0**

→ Pas de solution réelle.

**Conclusion : f'(x) = 0 uniquement pour x = 1/3**

---

## Le piège à éviter

Beaucoup d'élèves oublient de vérifier si le facteur intérieur peut s'annuler. Ici, 3x² − 2x + 1 > 0 pour tout x (discriminant négatif + coefficient directeur positif), donc seul 3x − 1 = 0 donne une solution.

---

Tu veux t'entraîner sur d'autres exercices du même type ? Je publie régulièrement des corrigés détaillés. Et pour un accompagnement personnalisé, c'est par là 👇
