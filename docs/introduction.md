---
title: ''
sidebar_position: 1
---

<p align="center">
  <img src="/img/logo-white-border.svg" width="400px"/>


[![Latest Version on Packagist](https://img.shields.io/packagist/v/nutgram/nutgram.svg?style=flat-square)](https://packagist.org/packages/nutgram/nutgram)
[![Maintainability](https://api.codeclimate.com/v1/badges/86c4ca3dae8f64db80f7/maintainability)](https://codeclimate.com/github/nutgram/nutgram/maintainability)
[![Total Downloads](https://img.shields.io/packagist/dt/nutgram/nutgram.svg?style=flat-square)](https://packagist.org/packages/nutgram/nutgram)
[![License](https://poser.pugx.org/nutgram/nutgram/license)](//packagist.org/packages/nutgram/nutgram)

</p>

> The Telegram bot library that doesn't drive you nuts

Taking advantage of the **PHP8** features, this framework and tries to make the **speed**, **scalability** and **flexibility** of use its strength, allowing to quickly make simple bots, but at the same time, it provides
more **advanced features** to handle even the most complicated flows. Some architectural concepts on which
Nutgram is based are heavily influenced by other open source projects such as [Botman](https://github.com/botman/botman)
and [Zanzara](https://github.com/badfarm/zanzara).

```php
<?php

use SergiX44\Nutgram\Nutgram;

$bot = new Nutgram($_ENV['TOKEN']);

$bot->onCommand('start', function(Nutgram $bot) {
    $bot->sendMessage('Ciao!');
});

$bot->onText('My name is {name}', function(Nutgram $bot, string $name) {
    $bot->sendMessage("Hi $name");
})

$bot->run();

```
