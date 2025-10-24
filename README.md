# Docker LEMP Stack with phpMyAdmin

This is a complete Docker Compose configuration for a LEMP (Nginx, MariaDB, PHP) stack, which also includes phpMyAdmin for easy database management.

This project is structured to use a `.env` file for all passwords and sensitive information, so you can safely commit the repository to GitHub without exposing your credentials.

## Services Included

| Service | Image | Host Port |
| :--- | :--- | :--- |
| **Nginx** | `nginx:1.25-alpine` | `:80` |
| **PHP** | `php:8.2-fpm-alpine` | `(none)` |
| **MariaDB** | `mariadb:10.11` | `(none)` |
| **phpMyAdmin** | `phpmyadmin:5.2` | `:8080` |

---

## ⚡ How to Deploy

### 1. Clone the Repository
```sh
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name