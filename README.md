# Laravel 11 SPA with Turbolinks

This project shows how to simulate a Single Page Application (SPA) in Laravel 11 using [Turbolinks](https://github.com/turbolinks/turbolinks), without needing Vue or React.# laravel-turbolinks

## ⚙️ Features

- Laravel 11 with Vite
- Turbolinks for SPA-like experience
- Fast navigation without full reloads
- Simple Blade-based layout
- No Vue/React required

## 🚀 Installation Guide

composer create-project laravel/laravel laravel-turbolinks-spa
cd laravel-turbolinks-spa

2. Install dependencies
composer install
npm install

3. Setup Environment

cp .env.example .env
php artisan key:generate


4. Run the app
Start Laravel backend:
php artisan serve

In a separate terminal, run frontend:
npm run dev
Open in browser:
➡️ http://127.0.0.1:8000

Turbolinks Setup (Step-by-Step)
✅ Step 1: Install Turbolinks
npm install turbolinks


Step 2: Add Turbolinks to resources/js/app.js
import './bootstrap';
import Turbolinks from 'turbolinks';

Turbolinks.start();

document.addEventListener("turbolinks:load", () => {
    console.log("Turbolinks loaded!");
});


Step 3: Update Layout File resources/views/layouts/app.blade.php
<meta name="turbolinks-cache-control" content="no-cache">
@vite(['resources/css/app.css', 'resources/js/app.js'])

✅ Step 4: Create Blade Views
In routes/web.php:
Route::get('/', fn() => view('welcome'));
Route::get('/about', fn() => view('about'));
Route::get('/contact', fn() => view('contact'));

📁 Folder Structure (Important Parts)
laravel-turbolinks-spa/
├── resources/
│   ├── js/app.js
│   └── views/
│       ├── layouts/app.blade.php
│       ├── welcome.blade.php
│       ├── about.blade.php
│       └── contact.blade.php
├── routes/web.php
├── README.md ✅


👨‍💻 Author
Hamza Khan
GitHub: @hamzakhan123

