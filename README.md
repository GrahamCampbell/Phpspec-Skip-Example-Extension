# Phpspec Skip Example Extension

This Phpspec extension allows to skip example through user-friendly annotations.

## Installation

```
$ composer require "graham-campbell/phpspec-skip-example-extension:^5.1"
```

## Configuration

You can now activate the extension by creating a `phpspec.yml` file at the root of your project:

``` yaml
extensions:
    Akeneo\SkipExampleExtension: ~
```

## Usage

### @require <class or interface>

Skips all the spec example if the class or interface is not available

```php
/**
 * @require Vendor\Builder\ToolInterface
 */
class BridgeBuilderSpec extends ObjectBehavior
{
    // Will be skipped if the Vendor\Builder\ToolInterface interface does not exist
    function it_builds_a_brige()
    {
    }

    // Will be skipped if the Vendor\Builder\ToolInterface interface does not exist
    function it_builds_the_road()
    {
    }

    //...
}
```

## Contributions

Feel free to contribute to this extension if you find some interesting ways to improve it!
