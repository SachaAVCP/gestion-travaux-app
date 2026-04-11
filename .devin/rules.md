# Règles Devin — Gestion Travaux App

## Règle n°1 : Consultation obligatoire des playbooks

À chaque nouvelle tâche, AVANT de commencer à coder, tu DOIS :

1. Lire systématiquement `README.md` s'il existe.
2. Identifier le type de tâche et exécuter le playbook correspondant :

| Type de tâche | Playbook à exécuter |
|---|---|
| **Feature / nouvelle fonctionnalité** | `!Feature_development` |
| **Bug / debug / correction** | `!Debug` |
| **Refactor / restructuration** | `!safe_refactor` |

3. Si un document de référence existe dans le repo pour le sujet (ex: `feature-plan-*.md`, `refactor-plan-*.md`, `debug_analysis.md`, `ANALYSE_*.md`), le lire EN ENTIER avant de coder.
4. Si aucun playbook ni document ne correspond à la tâche, le signaler à l'utilisateur et proposer un plan avant de coder.

**Ne commence JAMAIS à écrire du code sans avoir exécuté le playbook adapté.**
