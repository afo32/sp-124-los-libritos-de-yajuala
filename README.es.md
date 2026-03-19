# 📚 Los Libritos de Yajuala

Aplicación web full-stack para la gestión de libros, construida con **React.js** en el frontend y **Python/Flask** en el backend. Desarrollada como proyecto grupal de [4Geeks Academy](https://4geeksacademy.com/).

---

## 🚀 Stack Tecnológico

| Capa | Tecnología |
|------|------------|
| Frontend | React.js, Vite, CSS |
| Backend | Python, Flask, SQLAlchemy |
| Base de datos | PostgreSQL (también compatible con SQLite / MySQL) |
| Gestión de paquetes | Pipenv (Python) / npm (JS) |
| Despliegue | Render.com |

---

## ⚙️ Instalación y Configuración

### Requisitos previos

- Python 3.10+
- Node.js 20+
- PostgreSQL (recomendado) u otro motor de base de datos compatible
- Pipenv

---

### 🔧 Configuración del Backend

1. Instalar dependencias de Python:
   ```bash
   pipenv install
   ```

2. Crear el archivo de entorno:
   ```bash
   cp .env.example .env
   ```

3. Configura `DATABASE_URL` en tu `.env` según tu motor de base de datos:

   | Motor | DATABASE_URL |
   |-------|--------------|
   | SQLite | `sqlite:////test.db` |
   | MySQL | `mysql://username:password@localhost:port/example` |
   | PostgreSQL | `postgres://username:password@localhost:5432/example` |

4. Ejecutar las migraciones:
   ```bash
   pipenv run migrate
   pipenv run upgrade
   ```

5. Iniciar el servidor backend:
   ```bash
   pipenv run start
   ```

> **Usuarios de Codespaces:** Conéctate a PostgreSQL con:
> ```bash
> psql -h localhost -U gitpod example
> ```

---

### 🎨 Configuración del Frontend

1. Instalar dependencias de JavaScript:
   ```bash
   npm install
   ```

2. Iniciar el servidor de desarrollo:
   ```bash
   npm run start
   ```

---

## 🧪 Pruebas y Datos de Ejemplo

### Insertar usuarios de prueba

```bash
flask insert-test-users 5
```

### Insertar datos personalizados

Edita la función `insert_test_data` en `src/api/commands.py` y luego ejecuta:

```bash
pipenv run insert-test-data
```

> ⚠️ Cada entorno de GitHub Codespaces tiene su propia base de datos aislada. Los datos no persisten entre entornos.

---

## ↩️ Revertir una Migración

```bash
pipenv run downgrade
```

---

## 🌐 Despliegue

El proyecto está listo para desplegarse en **Render.com**. Sigue la [guía oficial de despliegue](https://4geeks.com/docs/start/deploy-to-render-com).

---

## 📁 Estructura del Proyecto

```
sp-124-los-libritos-de-yajuala/
├── src/
│   ├── api/          # Backend Flask (modelos, rutas, comandos)
│   └── front/        # Frontend React (componentes, páginas, estilos)
├── migrations/       # Migraciones de base de datos con Alembic
├── public/           # Recursos estáticos
├── .env.example      # Plantilla de variables de entorno
├── Pipfile           # Dependencias de Python
├── package.json      # Dependencias de JavaScript
└── render.yaml       # Configuración de despliegue en Render
```

---

## 👥 Colaboradores

Desarrollado por el equipo **Los Libritos de Yajuala** como parte del Bootcamp Full Stack de 4Geeks Academy (Grupo sp-124).

Plantilla original creada por [Alejandro Sanchez](https://twitter.com/alesanchezr) y colaboradores de [4Geeks Academy](https://github.com/4geeksacademy/).

---

## 📄 Licencia

Este proyecto es de código abierto y está disponible bajo la [Licencia MIT](LICENSE).
