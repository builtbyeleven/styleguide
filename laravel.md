## Laravel

### PHP

Follow the [PSR-2](https://www.php-fig.org/psr/psr-2/) unless there is a good reason to justify. Once approved by the team, update this style guide for future reference. Use [EditorConfig](https://editorconfig.org/) for your favorite editor.

### Routing

Public facing URLs must use kebab-case.

```
https://builtbyeleven.com/style-guide
https://pay.builtbyeleven.com/select-source-of-payment
```

A route URL must start with `/` (slash) unless it is an empty URL

```php
Route::get('/', 'HomeController@index');
Route::get('hello', 'HelloController@index');
```

Route name must use kebab-case

```php
Route::get('style-guide', 'StyleGuideController@index')->name('style-guide.index');
```

```blade
<a href="{{ route('style-guide.index') }}">
    Style Guide
</a>
```

Route parameters should use camelCase.

```php
Route::get('invoice/{invoiceId}', 'InvoiceController@show');
```

### Controller

Keep the controller to the default CRUD. Refactor the controller if it goes beyond it.

### View

The folder name must be the same as the route name. 

```php
Route::get('style-guide', 'StyleGuideController@index')->name('style-guide.index');
```

```
resources
  |- views
    |- style-guide/index.blade.php
```
