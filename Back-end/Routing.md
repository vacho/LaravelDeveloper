Routing
===
The code goes into Routes>name_file.php

--
```php
use Illuminate\Support\Facades\Route;
use Illuminate\Http\Request;

Route::get('/', function () {
    return view('welcome');
});

Route::get('/hello', function () {
   return response("<h1>Hello World</h1>", 200)
       ->header('Content-Type', 'text/html');
});

Route::get('/hello-view', function () {
    return view('hello');
});

Route::get('/post/{id}', function ($id) {
    //ddd($id);
    return view('post', ['id' => $id]);
})->where(['id' => '[0-9]+']);

Route::get('/search', function (Request $request) {
    dd($request);
});

Route::get('/json', function () {
    return response()->json([
        'people' => [
            [
                'name' => 'John',
                'surname' => 'Doe',
            ],
            [
                'name' => 'Jim',
                'surname' => 'Villa',
            ]
        ]
    ]);

});

```