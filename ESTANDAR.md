# Estándar de codificación Equipo 3

Lenguaje(s) del proyecto formativo:

## 1. Nombrado
(pendiente)

## 2. Formato
(pendiente)

## 3. Comentarios y documentación
(pendiente)

## 4. Estructura de carpetas
(pendiente)

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
