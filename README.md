# php-static-router
PHP Basic and Static Router


# Install
Requires PHP 7.4 or newer.

# Usage
Here's a basic usage example:

### Environment Setup: 

```
Set Your Website Url Via "Config/site.php
```

### Defining Routes:  

``` 
Navigate to "config/routes.php" to start defining your routes 
```

### Basic Usage:

Create Router Instance In "public/index.php" directory:

```
<?php
declare(strict_types=1);
ERROR_REPORTING(E_ALL);

require_once realpath("../vendor/autoload.php");
use FosterRouter\Router\Router;

$route = new Router();
require $route->routepath("routes");
```
<br>

Request With Static Pages:   

```
$route->get('/', 'index');
```
> Static Pages Can Be Created Via The "views" directory.  

<br>

### ``GET`` Requests With Callback: 

```
$route->get('/callback', function(){
    echo "Callback Test";
});
```

### ``POST`` Requests: 
```
$route->post('/demo', function(){
    echo "POST Request Test";
});
```


### ``PUT`` Request:

```
$route->put('/demo', function(){
    echo "PUT Request Test";
});
```


### ``Delete`` Request:
```
$route->delete('/demo', function(){
    echo "DELETE Request Test";
});
```

### ``[GET, POST, PUT, DELETE]`` Requests:
```
$route->any("/404", "404");

```




