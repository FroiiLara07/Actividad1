# Proyecto en Equipo — Sitio Web con Control de Versiones

Sitio web de 4 secciones desarrollado en equipo usando Git y GitHub, con una
rama independiente por integrante e integración vía Pull Request.

## Estructura del repositorio

```
├── index.html              # Página principal (punto de entrada)
├── assets/
│   ├── css/estilos.css     # Estilos compartidos (usados por index y las secciones)
│   └── js/                 # JS compartido si se necesita
├── seccion1/index.html     # Sección del integrante 1
├── seccion2/index.html     # Sección del integrante 2
├── seccion3/index.html     # Sección del integrante 3
└── seccion4/index.html     # Sección del integrante 4
```

Cada sección ya tiene:
- Un botón "← Regresar al inicio" que apunta a `../index.html`.
- Un enlace correspondiente en `index.html`.

**Regla:** cada integrante solo edita el contenido dentro de su propia carpeta
`seccionX/`. Si necesitan un CSS o JS propio, créenlo dentro de su misma
carpeta (ej. `seccion1/estilos.css`) para evitar pisar el trabajo de los
demás en `assets/`.

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
