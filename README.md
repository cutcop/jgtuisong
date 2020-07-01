# push

## Introduction

Third party message push

## Install

```
$ composer require cutcop/jgtuisong
```

## Demo

```php
<?php

require __DIR__ . '/vendor/autoload.php';

$appKey = 'your-app-key';
$masterSecret = 'your-master-secret';

$alert = 'Hi JPush!';
$extras = [
    'type' => 1,
    'url' => ''
];
$platform = ['android', 'ios'];
$audience = [
    'alias' => ['13888888888']
];

$push = new Cutcop\Jgtuisong\JPush($appKey, $masterSecret);
$push->push($alert, $extras, $platform, $audience);
```