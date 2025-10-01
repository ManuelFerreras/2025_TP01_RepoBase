# Decisiones del TP01 – Git Básico (2025)

## Configuración

```bash
git config --global user.name "Manuel Ferreras"
git config --global user.email "manuel.ferreras1@gmail.com"
git config --global init.defaultBranch main
```

Dejé constancia de mi identidad para trazabilidad.

## Flujo de trabajo

- `main` → rama estable.
- `feat/despedida` → nueva funcionalidad.
- `hotfix/saludo-fix` → arreglo urgente.

## Funcionalidad

Agregué función `despedir()` en `src/app.js` y luego la invoqué.
Dos commits atómicos:

1. agregar función
2. invocar función

## Hotfix

Simulé bug en `saludar()`.
Arreglo en `hotfix/saludo-fix`:

- a `main` lo integré con **merge**
- a la feature lo llevé con **cherry-pick**

## Pull Request

Abrí un PR desde `feat/despedida` hacia `main` y lo mergeé con **merge commit**.

## Versión estable

Creé el tag:

```bash
git tag -a v1.0 -m "Stable v1.0: saludar + despedir con hotfix"
git push origin v1.0
```
