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
(pendiente)

## 3. Comentarios y documentación
(pendiente)

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
(pendiente)
