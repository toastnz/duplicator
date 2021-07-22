# SilverStripe Duplicator

Simple module to duplicate relationships by hard-copying them when duplicating objects

## Requirements

See composer.json

## Usage

Define which relationships should be duplicated in the `config.yml`:

```yaml
Page:
  duplicator_relations:
    - Slides
```

Or directly in the class:

```php
<?php

class Page extends SiteTree
{
    private static $many_many = [
        'Slides' => Slide::class
    ];
    
    private static $duplicator_relations = [
        'Slides'
    ];
    
}
```
