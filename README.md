# Docker LEMP Stack (Nginx, MariaDB, PHP + phpMyAdmin)

This repository provides a `docker-compose.yml` file to quickly launch a full web development environment.

## 🚀 Quick Start

1.  Clone the repo: `git clone https://github.com/your-username/your-repo-name.git`
2.  `cd your-repo-name`
3.  `cp .env.example .env`
4.  Edit the `.env` file with your secure passwords.
5.  `docker compose up -d`

---

## 📋 Project Overview

### Services

* **`nginx`**: Nginx 1.25 (Alpine)
* **`php`**: PHP 8.2 (FPM-Alpine)
* **`mariadb`**: MariaDB 10.11
* **`phpmyadmin`**: phpMyAdmin 5.2

### Required File Structure

To run this stack, your project folder **must** be organized like this:

```plaintext
.
├── .env.example        # Template for environment variables
├── .gitignore          # Prevents secrets from being committed
├── docker-compose.yml  # The main stack file (uses variables from .env)
│
├── app/                # <-- Your PHP application code goes here
│   └── index.php
│
└── nginx/              # <-- Nginx configuration
    └── default.conf
```

## ⚙️ Step-by-Step Setup
### Step 1: Clone the Repository
```Bash

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```
### Step 2: Configure Your Environment
This project uses a .env file to keep your passwords secure and out of GitHub.

1. Copy the example file:

```Bash
cp .env.example .env
```
2. Open the new .env file with a text editor and set your own secure passwords.

### Step 3: Add Your PHP Code
Place your website's files (e.g., index.php, config.php, etc.) into the ./app/ directory.

### Step 4: Deploy the Stack
Run the following command from your project's root directory:

```Bash
docker compose up -d
```
## 💻 Accessing Your Services
* #### Your Website:
  * URL: http://localhost
* #### phpMyAdmin (Database Manager):
  * URL: http://localhost:8080
  * Server: mariadb
  * Username: root
  * Password: (The MYSQL_ROOT_PASSWORD you set in your .env file)

## 🔒 Security
The .gitignore file is configured to ignore your local .env file. This is crucial for security. Never commit your .env file to GitHub.

---

After you replace the text in your `README.md` file, you can update it on GitHub with these commands:

```sh
git add README.md
git commit -m "Fix README formatting"
git push
```