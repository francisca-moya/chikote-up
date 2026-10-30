# Cómo contribuir a Chikote Up

Este documento explica cómo nos organizamos para trabajar en el proyecto y cómo subir los cambios al repositorio. La idea es que todos sigamos unas mismas pautas para evitar problemas y mantener el trabajo ordenado.

## Ramas del proyecto

Vamos a trabajar con cuatro ramas fijas. Cada miembro tendrá asignada una rama según la parte del proyecto en la que trabaje. No se crearán ramas nuevas.

- `main`: contiene la versión estable del proyecto. Los cambios se incorporan mediante pull request.
- `design/frontend`: HTML, CSS y JavaScript dentro de la carpeta `design/`. Responsable: [@francisca-moya](https://github.com/francisca-moya)
- `[nombre-rama-2]`: [parte del proyecto]. Responsable: [@usuario].
- `[nombre-rama-3]`: [parte del proyecto]. Responsable: [@usuario].

Cada persona debe trabajar en su rama y evitar subir cambios directamente a las ramas de los demás.

## Cómo subir cambios

Para empezar a trabajar, hay que situarse en la rama correspondiente y actualizarla con los últimos cambios de `main`:

```bash
git switch nombre-rama
git fetch origin
git merge origin/main
```

Después, se trabaja con normalidad y se guardan los cambios mediante commits. Para subir el trabajo al repositorio:

```bash
git push origin nombre-rama
```

Cuando los cambios estén listos, se abre un pull request desde la rama de trabajo hacia `main`. Es recomendable hacer commits pequeños y subir los cambios con frecuencia, en lugar de acumular mucho trabajo para el final.

## Pull requests

Al abrir un pull request:

  - Hay que indicar brevemente qué cambios se han realizado.
  - Se debe utilizar la plantilla automática del repositorio [pull_request_template.md](`.github/pull_request_template.md`).
  - Hay que comprobar que los cambios funcionan antes de solicitar la revisión.
  - Otra persona del equipo debe revisar los cambios antes de integrarlos en main.
  - Si se encuentra algún problema, se corrige antes de aceptar el pull request.

## Commits

Los mensajes de los commits deben ser breves y explicar claramente qué se ha hecho. Utilizaremos el castellano y, siempre que sea posible, verbos en infinitivo.

**Ejemplos:**

  - Añadir formulario de registro
  - Crear vista de recetas
  - Corregir estilos del menú
  - Actualizar documentación

## Estilo del proyecto

Para mantener una apariencia coherente en toda la aplicación, seguiremos las indicaciones de la [guía de estilo](docs/guia-de-estilo.md), donde se recogen los colores, las tipografías y las variables CSS del proyecto.

## Errores y nuevas propuestas

Si encontramos un error o queremos proponer una funcionalidad, utilizaremos las plantillas de **issues** disponibles en `.github/ISSUE_TEMPLATE/`:

  - [bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md): para informar de errores.
  - [feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md): para proponer nuevas funcionalidades o mejoras.

## Seguridad

No se deben subir contraseñas, claves de API, archivos .env ni ningún otro dato privado al repositorio. Si se sube una clave por error, hay que avisar al equipo y revocarla cuanto antes. Borrarla del repositorio no garantiza que deje de estar expuesta.
