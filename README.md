# Sitio informativo de la universidad

Sitio web institucional (tema naranja y blanco) desarrollado en equipo usando
Git y GitHub, con una rama independiente por integrante e integración vía
Pull Request.

## Responsables por sección

| # | Sección                  | Responsable | Carpeta      |
|---|---------------------------|-------------|--------------|
| 1 | Carreras                  | Juan        | `seccion1/`  |
| 2 | Requisitos de admisión    | Carlos      | `seccion2/`  |
| 3 | Actividades                | Missael     | `seccion3/`  |
| 4 | Servicios                  | Angel       | `seccion4/`  |

El `index.html` (página principal) lo maneja Froy.

## Estructura del repositorio

```
├── index.html               # Página principal (punto de entrada)
├── assets/
│   ├── css/estilos.css      # Estilos compartidos (nav, footer, tema naranja/blanco)
│   ├── img/                 # Logo institucional
│   └── js/                  # JS compartido si se necesita
├── seccion1/index.html      # Carreras — Juan
├── seccion2/index.html      # Requisitos de admisión — Carlos
├── seccion3/index.html      # Actividades — Missael
└── seccion4/index.html      # Servicios — Angel
```

Cada página de sección ya trae el **nav** y el **footer** iguales al resto del
sitio (no se tocan). Adentro hay una nota tipo `placeholder-nota` marcando
dónde va el contenido — bórrenla al agregar el suyo.

**Regla:** cada integrante solo edita el contenido dentro de su propia carpeta
`seccionX/`, entre el nav y el footer. No modifiquen `assets/css/estilos.css`
directamente (es compartido); si necesitan un estilo extra muy específico de
su sección, agréguenlo en un `<style>` dentro de su propio `index.html`.

## Flujo de trabajo en Git (obligatorio para todos)

1. **Clonar el repositorio** (una sola vez):
   ```bash
   git clone <URL-DEL-REPOSITORIO>
   cd <nombre-del-repo>
   ```

2. **Actualizar `main` antes de empezar:**
   ```bash
   git checkout main
   git pull origin main
   ```

3. **Crear tu rama personal** a partir de `main` (usa tu nombre o "seccionX"):
   ```bash
   git checkout -b seccion1-nombre
   ```

4. **Trabajar solo en tu carpeta** (`seccion1/`, `seccion2/`, etc.) y hacer
   commits frecuentes y descriptivos:
   ```bash
   git add seccion1/
   git commit -m "Agrega contenido inicial de la sección 1"
   ```

5. **Subir tu rama a GitHub:**
   ```bash
   git push origin seccion1-nombre
   ```

6. **Abrir un Pull Request** en GitHub de `seccion1-nombre` hacia `main`,
   pedir revisión de un compañero, y hacer el **merge** una vez aprobado.

7. **Después del merge**, todos deben volver a sincronizar su `main` local:
   ```bash
   git checkout main
   git pull origin main
   ```

## Para la presentación

- **Ramas:** en GitHub → pestaña "Branches" se ve una rama por integrante.
- **Commits:** en GitHub → "Insights → Contributors" o el historial de commits
  de cada rama/PR muestra la participación individual.
- **Pull Requests:** pestaña "Pull requests" (incluyendo los ya cerrados/mergeados)
  muestra la integración de cada sección a `main`.
- **Sitio funcionando:** activar GitHub Pages (Settings → Pages → rama `main`,
  carpeta `/root`) y compartir la liga que genera.
