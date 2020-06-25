# Laravel Nova Editor JS Field

[![Latest Version on Github](https://img.shields.io/github/release/advoor/nova-editor-js.svg?style=flat-square)](https://packagist.org/packages/advoor/nova-editor-js)
[![Total Downloads](https://img.shields.io/packagist/dt/advoor/nova-editor-js.svg?style=flat-square)](https://packagist.org/packages/advoor/nova-editor-js)

This package was forked from `https://github.com/advoor/nova-editor-js`. This package was forked to bump the Nova version to 3.0+.

A Laravel Nova implementation of [Editor.js](https://github.com/codex-team/editor.js) by [@advoor](https://github.com/advoor).

## Installation

Install via composer:

```
composer require advoor/nova-editor-js
```

Publish the config file
```
php artisan vendor:publish --provider="MattadorStarfish\NovaEditorJs\FieldServiceProvider"
```

## Upgrade
If upgrading from v0.4.0, re-publish the config file!

## Usage:

Add this `use` statement to the top of the your nova resource file:

```
use MattadorStarfish\NovaEditorJs\NovaEditorJs;
```

Use the field as below:

```
NovaEditorJs::make('FieldName')
```

And boom!

You can configure what tools the Editor should use in the config 
file along with some other settings so make sure to have a look :)

You can use the built in function to generate the response for the frontend:

```
NovaEditorJs::generateHtmlOutput($user->about);
```

Each 'block' has it's own view which can be overwritten in `resources/views/vendor/nova-editor-js/`

## Tools included
* https://github.com/editor-js/header
* https://github.com/editor-js/image
* https://github.com/editor-js/code
* https://github.com/editor-js/link
* https://github.com/editor-js/list
* https://github.com/editor-js/inline-code
* https://github.com/editor-js/checklist
* https://github.com/editor-js/marker
* https://github.com/editor-js/embed
* https://github.com/editor-js/delimiter
* https://github.com/editor-js/table
* https://github.com/editor-js/raw