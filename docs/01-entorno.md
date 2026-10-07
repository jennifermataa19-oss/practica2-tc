# Ejercicio 1. Entorno de trabajo y flujo de ramas

## Reutilización de la Práctica 1

Para esta práctica se reutilizó el entorno desarrollado en la Práctica 1.

Se copiaron los siguientes elementos:

- `entorno/Dockerfile`
- `entorno/compose.yml`
- `requirements.txt`
- `pytest.ini`
- `src/lenguajes.py`
- `tests/test_lenguajes.py`

El módulo `lenguajes.py` contiene las operaciones sobre cadenas y lenguajes implementadas previamente, por lo que no fue necesario volver a desarrollarlas.

Repositorio de la Práctica 1:

https://github.com/jennifermataa19-oss/flet-docker

## Flujo de trabajo con Git

La Práctica 2 utiliza una rama independiente para cada funcionalidad.

El flujo utilizado es:

1. Partir de la rama `main`.
2. Crear una rama para la funcionalidad.
3. Realizar los cambios.
4. Crear uno o más commits.
5. Subir la rama a GitHub.
6. Crear un Pull Request.
7. Fusionar el Pull Request con `main`.
8. Actualizar la rama local `main`.

Ejemplo:

```bash
git switch main
git pull
git switch -c feature/nueva-funcionalidad
git add .
git commit -m "Descripcion del cambio"
git push -u origin feature/nueva-funcionalidad
```

## Integración continua

Se configuró GitHub Actions para ejecutar automáticamente las pruebas del proyecto con las siguientes versiones de Python:

- Python 3.11
- Python 3.12
- Python 3.13

El flujo se encuentra en:

`.github/workflows/pruebas.yml`

Las pruebas se ejecutan con:

```bash
pytest -q
```

## Evidencias

Las evidencias del Ejercicio 1 se almacenarán dentro de las carpetas correspondientes en `evidencias/`.

Se incluirán las siguientes evidencias:

- Dirección del repositorio.
- Captura de `git log --oneline --graph --all`.
- Captura de la lista de Pull Requests cerrados.
- Captura de GitHub Actions con las pruebas aprobadas en Python 3.11, 3.12 y 3.13.