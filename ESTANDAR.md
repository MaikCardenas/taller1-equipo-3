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
```
proyecto/
├── docs/            # documentación, diagramas y manuales
├── src/             # código fuente
│   ├── controladores/
│   ├── modelos/
│   └── vistas/
├── public/          # archivos accesibles desde el navegador
│   ├── css/
│   ├── js/
│   └── img/
├── database/        # scripts SQL (creación de tablas y datos de prueba)
├── tests/           # pruebas
├── visitas/         # visitas de otros equipos
├── .editorconfig
├── ESTANDAR.md
└── README.md
```

Reglas: nombres de carpetas en minúscula y sin tildes; cada carpeta tiene una sola responsabilidad; no se suben contraseñas ni archivos temporales (se usa `.gitignore`).

## 5. Git: ramas, commits y pull requests
**Ramas:** `tipo/descripcion-corta` en minúscula y con guiones.

| Tipo     | Uso                      |  Ejemplo               |
|----------|--------------------------|------------------------|
| feature  | funcionalidad nueva      | feature/login-usuarios |
| fix      | corrección de errores    | fix/ortografia-readme  | 
| docs     | documentación            | docs/estandar-git      |
| chore    | configuración y tareas   | chore/editorconfig     |

**Commits:** formato `tipo: descripción en presente`, máximo 72 caracteres. Ejemplo: `fix: corrige validación del formulario`. Si cierra un issue, se agrega `Closes #N`.

**Pull requests:**
- Nunca se trabaja directo en `main`; todo cambio entra por PR.
- Título igual al commit y `Closes #N` en la descripción.
- Otro integrante lo revisa y aprueba; nadie fusiona su propio PR.
- Se resuelven los conflictos antes de fusionar.

**Versiones:** versionamiento semántico MAYOR.MENOR.PARCHE (v1.0.0, v1.0.1).
