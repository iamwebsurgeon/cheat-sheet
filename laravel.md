# My Programming Cheatsheet
## Laravel
-  [Basics](https://github.com/iamwebsurgeon/cheat-sheet/blob/main/laravel.md#basics)
-  [Migrations](https://github.com/iamwebsurgeon/cheat-sheet/blob/main/laravel.md#migration)


### Basics
Clearing the configuration cache
```
php artisan config:clear
```
Reset configuration cache after clearing them
```
php artisan config:cache
```
Clear all route cache
```
php artisan route:clear
```
To cache your routes again
```
php artisan route:cache
```
Clear all compiled views cache
```
php artisan view:clear
```
Clears the view cache before recompiling a new set of views
```
php artisan view:cache
```
To clear all Laravel's cache
```
php artisan optimize:clear
```
List available Artisan commands
```
php artisan list
```
Set database string
```
Update your /app/Providers/AppServiceProvider.php to contain:
use Illuminate\Support\Facades\Schema;
public function boot()
{
    Schema::defaultStringLength(191);
}
```
### Migration
For migrating specific migration file
```
php artisan migrate:refresh--path=database/migrations/2021_05_01_092040_create_products_table.php
```



