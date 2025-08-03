# Symfony 6.4 Fast Track Demo

A demo Symfony 6.4 application based on [The Symfony Fast Track Book](https://symfony.com/doc/6.4/the-fast-track/en/index.html). It features a full-stack Symfony setup with Docker, PostgreSQL, Messenger, Mailer, and more.

## 📦 Features

- Symfony 6.4 (LTS)
- Docker-based local dev environment
- PostgreSQL via Docker
- Mailer with [Mailpit](https://github.com/axllent/mailpit) for testing email delivery
- Symfony Flex, MakerBundle, Twig, API Platform (optional)
- Configuration via `.env`
- Environment-ready for production

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/symfony-fast-track-demo.git
cd symfony-fast-track-demo
```

### 2. Start Docker containers
Make sure Docker is running on your machine, then:

```bash
docker compose up -d
```
This will start:
- Symfony app
- PostgreSQL
- Mailpit (for email viewing)

📌 If you get an error like:
```
Cannot connect to the Docker daemon...
```
make sure Docker Desktop is running.

## ⚙️ Configuration
Environment variables

Copy the example environment file:
```bash
cp .env .env.local
```

Edit database DSN if needed:
```ini
DATABASE_URL="pgsql://symfony:symfony@db:5432/app?serverVersion=15&charset=utf8"
```

## 🗃️ Database Setup
Run database migrations:
```bash
docker compose exec php bin/console doctrine:database:create
docker compose exec php bin/console doctrine:migrations:migrate
```

(Optional) Load fixtures:
```bash
docker compose exec php bin/console doctrine:fixtures:load
```

## 📬 Mailer with Mailpit
Emails sent by Symfony are captured by Mailpit.

URL: http://localhost:8025

Send a test email:
```bash
docker compose exec php bin/console app:send-test-email
```

## 🧪 Useful Commands
```bash
docker compose exec php bash                  # Enter app container
docker compose exec php bin/console list      # View Symfony commands
docker compose exec php bin/phpunit           # Run tests (if configured)
```
---
### 📚 Reference
This project follows the official guide:

📖 Symfony Fast Track Book (6.4)

### 🤝 Credits
Symfony Core Team

Contributors to the book and documentation

Mailpit for local email testing

### 🛡 License
MIT — feel free to use, modify, and distribute.
