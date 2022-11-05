This Laravel Generator package provides and generate Controller, Model (with eloquent relations) and Views in **Bootstrap** for your development of your applications with single command.

- Will create **Model** with Eloquent relations
- Will create **Controller** with all resources
- Will create **views** in Bootstrap 
- It will also handle foreign key constraints and show select input in crud forms for foriegn key fields 

## Requirements
    Laravel >= 5.5
    PHP >= 7.1
    Mysql

## Installation
1 - Install
```
composer require ahnaf/crud-generator --dev
```
2- Publish the default package's config
```
php artisan vendor:publish --tag=crud
```

## Usage
```
php artisan make:crud {table_name}

php artisan make:crud employees
```

Add a route in `web.php`
```
Route::resource('employees', 'EmployeeController');
```
Route name in plural slug case.

#### Options
 - Custom Route
```
php artisan make:crud {table_name} --route={route_name}
```