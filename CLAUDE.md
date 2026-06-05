# CLAUDE.md — Règles permanentes Claude Code (AVCP)

Ce fichier est lu automatiquement par Claude Code à chaque exécution dans ce repo.
Il joue le rôle de "mémoire de projet" persistante (équivalent du LLM Wiki / knowledge notes côté Devin).

## Règles de branche & PR (NON NÉGOCIABLE)
- Toujours travailler sur la branche **`dev`** (staging). Ne jamais committer directement sur `main`.
- Toute modification passe par une **Pull Request vers `dev`**.
- La fusion `dev` → `main` (production) est **manuelle**, décidée par Sacha. Ne jamais la déclencher.
- Une PR = un sujet. Pas de PR fourre-tout.

## Périmètre autorisé
- ✅ Code applicatif, refactoring, audits, tests, documentation, correction de bugs.
- ❌ Aucune opération interactive sur l'infra H100 : pas de SSH, pas d'accès Dify DB, pas de Docker en prod, pas de manipulation de `.env` / secrets.

## Qualité (gates)
- Pas de fichier > 800 lignes (découper).
- Pas de `any` TypeScript non justifié.
- Pas de `console.log` / logs de debug laissés en place.
- Respecter le lint et les types existants ; lancer les tests si présents.

## Documentation
- Pour tout changement sur **AVCP Studio / Dify**, ajouter une section décrivant l'**Intégration dans le Studio Unifié** dans la description de PR.
- Pour les autres projets AVCP, ne pas ajouter cette section.

## Style de PR
- Titre clair en français, préfixe conventionnel (`feat:`, `fix:`, `refactor:`, `docs:`, `test:`).
- Description : contexte, ce qui change, fichiers touchés, comment tester, risques.
- Lier l'issue d'origine (`Closes #N`).
