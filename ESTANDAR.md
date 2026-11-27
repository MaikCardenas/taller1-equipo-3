# Estándar de codificación Equipo 3

Lenguaje(s) del proyecto formativo: TypeScript, JavaScript, Java (Spring Boot), SQL (PostgreSQL / PostGIS).

## 1. Nombrado

- **Language:** All code identifiers, files, folders, and database schemas/columns must be written in **English** (no accents or `ñ`).

| Element | Convention | Example |
| --- | --- | --- |
| Variables | `camelCase` | `speciesList` |
| Functions / Methods | `camelCase` (verb + noun) | `fetchSpeciesById()` |
| Classes / React Components | `PascalCase` | `SpeciesController`, `GlobeView` |
| Constants | `UPPER_SNAKE_CASE` | `DEFAULT_SUBSCRIPTION_PLAN` |
| Files (code / components) | `PascalCase` or `kebab-case` | `SpeciesCard.tsx`, `species-service.ts` |
| Folders | `kebab-case` | `species-catalog`, `auth-module` |
| Database tables & columns | `snake_case` (plural tables) | `species_sources`, `scientific_name` |

## 2. Formato

- **Indentation:** Use **2 spaces** (no tabs) for general code and configuration, aligned with `.editorconfig`.
- **Quotes:** Use **single quotes** (`'...'`) for strings in TypeScript/JavaScript and **double quotes** (`"..."`) in Java, JSON, and HTML/JSX attributes when standard.
- **Max line length:** Keep lines up to **100 characters** maximum whenever practical.
- **Braces:** Use opening braces `{` on the same line (K&R / standard style) and closing braces `}` on a new line.

## 3. Comentarios y documentación

- **When to comment:** Explain *why* a non-obvious decision, business rule, or workaround exists (for example, plan access checks or verified data source rules); avoid redundant comments that only repeat what the code already states.
- **How to document functions & endpoints:** Document public services, complex functions, and API endpoints with clear descriptions of parameters, return values, plan/role requirements, and error cases.
- **What `README.md` must include:** Project overview, tech stack (React, TypeScript, Globe.gl, Spring Boot, PostgreSQL/PostGIS), team members, setup/run instructions, environment variables, and a link to `ESTANDAR.md`.

## 4. Estructura de carpetas
## 4. Folder structure

```
project/
├── docs/            # documentation, diagrams and manuals
├── src/             # source code
│   ├── controllers/
│   ├── models/
│   └── views/
├── public/          # files accessible from the browser
│   ├── css/
│   ├── js/
│   └── img/
├── database/        # SQL scripts (table creation and test data)
├── tests/           # tests
├── visits/          # visits from other teams
├── .editorconfig
├── ESTANDAR.md
└── README.md
```

Rules: folder names are lowercase, without accents; each folder has a single responsibility; passwords and temporary files are never committed (use `.gitignore`).

## 5. Git: ramas, commits y pull requests
## 5. Git: branches, commits and pull requests

**Branches:** `type/short-description`, lowercase with hyphens.

| Type | Use | Example |
|------|-----|---------|
| feature | new functionality | feature/user-login |
| fix | bug fixes | fix/readme-typo |
| docs | documentation | docs/standard-git |
| chore | configuration and tasks | chore/editorconfig |

**Commits:** format `type: description in present tense`, maximum 72 characters. Example: `fix: correct form validation`. If it closes an issue, add `Closes #N`.

**Pull requests:**
- Never work directly on `main`; every change goes through a PR.
- Title equal to the commit message and `Closes #N` in the description.
- Another team member reviews and approves it; nobody merges their own PR.
- Conflicts are resolved before merging.

**Versions:** semantic versioning MAJOR.MINOR.PATCH (v1.0.0, v1.0.1).
