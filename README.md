# Laravel MakeSure

Easier tests for laravel

[![StyleCI](https://github.styleci.io/repos/162841027/shield?branch=master)](https://github.styleci.io/repos/162841027)
[![Build Status](https://travis-ci.org/imanghafoori1/laravel-makesure.svg?branch=master)](https://travis-ci.org/imanghafoori1/laravel-makesure)
<a href="https://scrutinizer-ci.com/g/imanghafoori1/laravel-makesure"><img src="https://img.shields.io/scrutinizer/g/imanghafoori1/laravel-makesure.svg?style=round-square" alt="Quality Score"></img></a>

This package tries to give you a more readable syntax to write 

### Installation



```

composer require imanghafoori/laravel-makesure --dev

```


### Usage

You can use it like this :



```php

  MakeSure::about($this)->
      ->sendingGetRequest('some-url')
      ->isRespondedWith()
      ->statusCode(402);

// Instead of writing this :

$this
    ->get('some-url')
    ->assertStatus(402);

```

You should start of with the `MakeSure` alias or the `Imanghafoori\MakeSure\Facades\MakeSure` Facade class like this:

```

MakeSure::about($this)->...

```

Note that for technical reasons you should always pass $this into the `about` method.


then you have access to all of these methods:

```

sendingPostRequest

sendingJsonPostRequest

sendingDeleteRequest

sendingJsonDeleteRequest

sendingPutRequest

sendingJsonPutRequest

sendingPatchRequest

sendingJsonPatchRequest

sendingGetRequest

sendingJsonGetRequest

```
