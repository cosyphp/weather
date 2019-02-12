<h1 align="center"> weather </h1>

<p align="center"> A weather SDK..</p>


## Installing

```shell
$ composer require cosyphp/weather -vvv
```

## Usage

```
<?php

require __DIR__ .'/vendor/autoload.php';

use Cosyphp\Weather\Weather;

$key = 'a775cc62fc87a9d0d9106d63b9397d41';

$w = new Weather($key);

echo "获取实时天气：\n";

$response = $w->getWeather('郑州');

echo json_encode($response, JSON_UNESCAPED_UNICODE | JSON_PRETTY_PRINT);

echo "\n\n获取天气预报：\n";

$response = $w->getWeather('郑州', 'all');
echo json_encode($response, JSON_UNESCAPED_UNICODE | JSON_PRETTY_PRINT);

echo "\n\n获取实时天气(XML)：\n";

echo $w->getWeather('深圳', 'base', 'XML');
```

## Contributing

You can contribute in one of three ways:

1. File bug reports using the [issue tracker](https://github.com/cosyphp/weather/issues).
2. Answer questions or fix bugs on the [issue tracker](https://github.com/cosyphp/weather/issues).
3. Contribute new features or update the wiki.

_The code contribution process is not very formal. You just need to make sure that you follow the PSR-0, PSR-1, and PSR-2 coding guidelines. Any new code contributions must be accompanied by unit tests where applicable._

## License

MIT