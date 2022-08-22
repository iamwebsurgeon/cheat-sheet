# My Programming Cheatsheet
## Laravel
-  [Basics](https://github.com/iamwebsurgeon/cheat-sheet/blob/main/laravel.md#basics)
-  [Migrations](https://github.com/iamwebsurgeon/cheat-sheet/blob/main/laravel.md#migration)


### Basics
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



