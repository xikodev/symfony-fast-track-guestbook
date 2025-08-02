# Symfony Fast Track Guestbook

This repository contains the full source code for the **Symfony Fast Track** guestbook application, built following the official Symfony 6.4 Fast Track book:

[Symfony The Fast Track (6.4)](https://symfony.com/doc/6.4/the-fast-track/en/index.html)

## Overview

The guestbook application demonstrates a modern Symfony project structure and best practices, including:

- Symfony 6.4 framework features
- Doctrine ORM for database interactions
- Twig templating engine
- Form handling and validation
- User-friendly interface with responsive design

## Installation

### Requirements

- PHP 8.1 or higher
- Composer
- Symfony CLI (recommended)
- A supported database (e.g., MySQL, SQLite, PostgreSQL)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/xikodev/symfony-fast-track-guestbook.git
   cd symfony-fast-track-guestbook
2. Install dependencies with Composer:
   ```bash
   composer install
   ```
3. Configure your environment variables by copying .env:
   ```bash
   cp .env .env.local
   ```
   Update .env.local with your database credentials.

4. Create and migrate the database schema:
   ```bash
   php bin/console doctrine:database:create
   php bin/console doctrine:migrations:migrate
   ```
5. Run the Symfony local server:
   ```bash
   symfony server:start
   ```
Visit http://localhost:8000 in your browser.
