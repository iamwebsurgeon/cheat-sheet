# My Programming Cheatsheet
## Laravel
-  [Basics](https://github.com/iamwebsurgeon/cheat-sheet/blob/main/laravel.md#basics)
-  [Migrations](https://github.com/iamwebsurgeon/cheat-sheet/blob/main/laravel.md#migration)

### Basics
Set database string
```
Update your /app/Providers/AppServiceProvider.php to contain:
use Illuminate\Support\Facades\Schema;
public function boot()
{
    Schema::defaultStringLength(191);
}
```
Install Jetstream Livewire Stack
```
composer require laravel/jetstream
```
Install Jetstream With Livewire
```
php artisan jetstream:install livewire
or
php artisan jetstream:install livewire --teams
```
Or, Install Jetstream With Inertia
```
php artisan jetstream:install inertia
php artisan jetstream:install inertia --teams
```

#Finalizing The Installation
```
npm install
npm run build
php artisan migrate
```

Route::get('/cache-clear', function() {
    Artisan::call('cache:clear');
    return "Cache is cleared";
});
Route::get('/optimize-clear', function() {
    Artisan::call('optimize:clear');
    return "Optimize Clear Successfully";
});
Route::get('/optimize', function() {
    Artisan::call('optimize');
    return "Optimize Successfully";
});

Route::get('/storage-link', function() {
    Artisan::call('storage:link');
    return "Storage Link has been created Successfully";
});
Route::get('/storage-link-php', function(){
    $target = storage_path('app/public');
    $link = public_path('/storage');
    symlink($target, $link);
    echo "symbolic link created successfully";
});
```
#### Cache
Clearing the configuration cache
```
php artisan config:clear
```
Reset configuration cache after clearing them
```
php artisan config:cache
```
#### Routes
Clear all route cache
```
php artisan route:clear
```
To cache your routes again
```
php artisan route:cache
```
#### Views
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
#### Others
List available Artisan commands
```
php artisan list
```
Storage Link
```
php artisan storage:link
```
Storage Link using PHP Function
```
Route::get('/storage-link-php', function(){
    $target = storage_path('app/public');
    $link = public_path('/storage');
    symlink($target, $link);
    echo "symbolic link created successfully";
});
```
```
### Migration
For migrating specific migration file
```
php artisan migrate:refresh --path=database/migrations/2021_05_01_092040_create_products_table.php
```

### Remove Public from Laravel Project using htaccess
```
<IfModule mod_rewrite.c>
   RewriteEngine On 
   RewriteRule ^(.*)$ public/$1 [L]
</IfModule>
```




