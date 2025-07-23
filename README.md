# Laravel 10 Installation & Common Commands

## ✅ Install Laravel 10

```
composer create-project --prefer-dist laravel/laravel:^10.0 your-project-name
```

## ✅ Run the Application

```
cd your-project-name
php artisan serve
```

---

## ✅ Create Views

> Laravel does not have `make:view` by default — create views manually or use an editor.

Example:

```
resources/views/common/header.blade.php
resources/views/home.blade.php
```

---

## ✅ Create Components

```
php artisan make:component MessageExample
```

- This creates:
  - `app/View/Components/MessageExample.php`
  - `resources/views/components/message-example.blade.php`

---

## ✅ Create Controllers

```
php artisan make:controller NameController
```

---

## ✅ Create Models

```
php artisan make:model Student
```

---

## ✅ Migrate Default Tables

```
php artisan migrate
```

---

## ✅ Show Model Info

```
php artisan model:show Student
```

---

## ✅ Publish Stubs

```
php artisan stub:publish
```

---

## ✅ Create Custom Validation Rule

```
php artisan make:rule Uppercase
```

---

## ✅ Create Middleware

```
php artisan make:middleware AgeCheck
```

---

## ✅ API Setup with Sanctum

1. Install Sanctum
   ```
   composer require laravel/sanctum
   ```

2. Use in `User` model:
   ```php
   use Laravel\Sanctum\HasApiTokens;

   class User extends Authenticatable
   {
       use HasApiTokens, HasFactory, Notifiable;
   }
   ```

3. Create API Controllers:
   ```
   php artisan make:controller API/AuthController
   php artisan make:model Post
   php artisan make:controller API/PostController
   ```

4. Install Guzzle HTTP client:
   ```
   composer require guzzlehttp/guzzle
   ```

---

## ✅ See Routes

```
php artisan route:list
```

---

## ✅ Create Service Classes

```
mkdir app/Services
php artisan make:class Services/JioCXEmailService
```

---

## ✅ Create Resource Controller for CRUD

```
php artisan make:controller ArticleController --resource
php artisan make:model Article -mc
```

- `-mc` creates Model, Controller, and Migration.

---

## ✅ Use Tinker

```
php artisan tinker
```

---

## ✅ Make Custom Artisan Command

```
php artisan make:command TestJioCXApi
```

---

## ✅ Install Authentication (Login, Register)

```
composer require laravel/breeze --dev
php artisan breeze:install blade
npm install
npm run dev
php artisan migrate
```

---

## ✅ Add Frontend Assets

Put your CSS and JS in:
```
public/css/style.css
public/js/main.js
```

Include in Blade:
```html
<link rel="stylesheet" href="{{ asset('css/style.css') }}">
<script src="{{ asset('js/main.js') }}"></script>
```

---

## ✅ Useful Authorization

Use `Bearer` token in API headers:
```
Authorization: Bearer <paste-your-token-here>
```

---

## ✅ Resource Test Example

```
php artisan make:controller ResourceTest --resource
```

---

## ✅ Example CRUD

```
php artisan make:model Article -mc
```

---
## ✅ URL OF LARAVEL
https://www.youtube.com/playlist?list=PL97P2RbKWLQgoJAoBbX_NpTMbs896ggWG
**Enjoy coding with Laravel 10 🚀**

