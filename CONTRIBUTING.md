# Contributing to Cruise Management System

Thank you for your interest in contributing to the **Cruise Management System**! This document provides global organization-wide guidelines for branching, commits, code quality, and pull requests across all repositories (`Cruise-api`, `Cruise-web`, `Cruise-pos`).

---

## 1. Branch Strategy

We follow a strict trunk-based / feature-branch workflow rooted on the latest `main`:

- **Branch naming convention**:
  - `feature/<JIRA-KEY>-<short-description>` (e.g. `feature/KAN-119-build-itinerary-ui`)
  - `bugfix/<JIRA-KEY>-<short-description>` (e.g. `bugfix/KAN-521-isolate-passenger-layout`)
  - `hotfix/<short-description>`
  - `chore/<short-description>`
- Always branch from the latest `origin/main`.
- Rebase on `origin/main` before opening or merging pull requests: `git fetch origin && git rebase origin/main`.

---

## 2. Conventional Commits

All commit messages across the organization must adhere to the Conventional Commits specification:

```
<type>(<scope>): <short description> (Refs: <JIRA-KEY>)
```

### Types:
- `feat`: A new feature
- `fix`: A bug fix
- `test`: Adding or refactoring tests
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `chore`: Changes to build scripts, CI configs, or dependencies

### Scopes:
- Backend: `api/activity`, `api/itinerary`, `api/pos`, `api/gateway`, `api/auth`
- Web: `ui/dashboard`, `ui/passenger`, `ui/pos`, `ui/excursions`, `ui/itinerary`
- Mobile POS: `pos/auth`, `pos/cart`, `pos/scanner`, `pos/shift`

---

## 3. Pull Request Guidelines

1. Every PR must use the organization Pull Request template (`.github/pull_request_template.md`).
2. Include the Jira issue reference in the title and description (e.g. `[KAN-120] feat: ...`).
3. Ensure all CI automated checks pass:
   - Backend: Maven targeted test suite, compilation, zero compiler warnings.
   - Frontend: Vitest suite, Oxlint check, Vite production build, SonarCloud quality gate.
   - Mobile: Gradle test and build.
4. Autonomous agents must never merge PRs into `main` without human user authorization.

---

## 4. Code Quality & Standards

- **Backend**: Java 21, Spring Boot 4.x, MapStruct compile-time mappers, strict validation (`@Valid`), zero raw System.out.
- **Frontend**: React 19, TypeScript strict mode, Tailwind CSS 4, zero memory leaks in WebGL/Canvas lifecycles.
- **Mobile POS**: Kotlin, Jetpack Compose, unidirectional data flow (UDF), offline-first SQLite/Room persistence.
