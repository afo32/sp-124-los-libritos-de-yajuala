# 📚 Los Libritos de Yajuala

A full-stack web application for book management, built with **React.js** on the frontend and **Python/Flask** on the backend. Developed as a group project at [4Geeks Academy](https://4geeksacademy.com/).

---

## 🚀 Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | React.js, Vite, CSS |
| Backend | Python, Flask, SQLAlchemy |
| Database | PostgreSQL (SQLite / MySQL supported) |
| Package Manager | Pipenv (Python) / npm (JS) |
| Deployment | Render.com |

---

## ⚙️ Installation & Setup

### Prerequisites

- Python 3.10+
- Node.js 20+
- PostgreSQL (recommended) or another supported DB engine
- Pipenv

---

### 🔧 Backend Setup

1. Install Python dependencies:
   ```bash
   pipenv install
   ```

2. Create your environment file:
   ```bash
   cp .env.example .env
   ```

3. Set your `DATABASE_URL` in `.env` according to your database engine:

   | Engine | DATABASE_URL |
   |--------|--------------|
   | SQLite | `sqlite:////test.db` |
   | MySQL | `mysql://username:password@localhost:port/example` |
   | PostgreSQL | `postgres://username:password@localhost:5432/example` |

4. Run database migrations:
   ```bash
   pipenv run migrate
   pipenv run upgrade
   ```

5. Start the backend server:
   ```bash
   pipenv run start
   ```

> **Codespaces users:** Connect to PostgreSQL with:
> ```bash
> psql -h localhost -U gitpod example
> ```

---

### 🎨 Frontend Setup

1. Install JavaScript dependencies:
   ```bash
   npm install
   ```

2. Start the development server:
   ```bash
   npm run start
   ```

---

## 🧪 Testing & Seeding Data

### Insert test users

```bash
flask insert-test-users 5
```

### Insert custom test data

Edit the `insert_test_data` function in `src/api/commands.py`, then run:

```bash
pipenv run insert-test-data
```

> ⚠️ Each GitHub Codespace has its own isolated database. Data will not persist between environments.

---

## ↩️ Undo a Migration

```bash
pipenv run downgrade
```

---

## 🌐 Deployment

This project is ready to deploy on **Render.com**. Follow the [official deployment guide](https://4geeks.com/docs/start/deploy-to-render-com).

---

## 📁 Project Structure

```
sp-124-los-libritos-de-yajuala/
├── src/
│   ├── api/          # Flask backend (models, routes, commands)
│   └── front/        # React frontend (components, pages, styles)
├── migrations/       # Alembic DB migrations
├── public/           # Static assets
├── .env.example      # Environment variable template
├── Pipfile           # Python dependencies
├── package.json      # JS dependencies
└── render.yaml       # Render deployment config
```

---

## 👥 Contributors

Built by the **Los Libritos de Yajuala** team as part of the 4Geeks Academy Full Stack Bootcamp (Group sp-124).

Template originally created by [Alejandro Sanchez](https://twitter.com/alesanchezr) and contributors at [4Geeks Academy](https://github.com/4geeksacademy/).

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
