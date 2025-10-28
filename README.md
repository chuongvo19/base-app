# Laravel Project - Base project

## Setup Project
Step 1: cd into base-app/infra and up docker
```bash
cd /base-app/infra
docker compose up --build -d
```
Step 2: Exec into container and setup
```bash
docker exec -it base-web-container bash
cp .env.example .env
composer install
php artisan migrate
php artisan make:filament-user
```
## ⚙️ Database Configuration

Dự án sử dụng **MySQL** làm cơ sở dữ liệu.  
Thông tin kết nối mặc định được cấu hình trong file `.env` như sau:

```env
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=db_pri
DB_USERNAME=user
DB_PASSWORD=password

URL App: http://example.com/
URL Admin: http://example.com/admin

Container backend: docker exec -it base-web-container bash
