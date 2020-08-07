# Coding Standards of WebFiori Framework

## Autoloading
The framework has its owon autoloader implementation which follows <a href="https://www.php-fig.org/psr/psr-4/" target="_blank">PSR-4</a> in almost all aspects of autoloading. There are some differences which are:

* The autoloader will throw `ClassLoaderException` if a class was not found.
* It is recomended that a fully qualified class name to have the following form: `vendorName\subNamespaceNames\ClassName` (names uses camleCase).

The framework can be configured to not throw an exception. This can be performed during the process of initializing the autoloader <a href="https://webfiori.com/docs/webfiori/entity/AutoLoader" target="_blank">AutoLoader</a>.

## Coding Style
It is recommended to follow the following rules while writing any PHP code. The rules are:

* Namespaces must be all `lower\case`.
* Class constants and global constants names must be decalred in `ALL_CAPS`.
* Methods names, non-static class attributes must be decalred in `camelCase`.
* Classed names and static attributes names must be decalred in `PascalCase`.
* An opening braces `{` must be on the same line for method and class declaration.
* Never use `elseif`. Always use `else if`.
* Always include access modifiers for class methods even if they are public.
* Private methods names should always start with underscore.

## Documentation Style
The PHPDoc block must be similar to the following style:
```
/**
 * SHORT_DESC.
 *
 * LONG_DESC
 * 
 * @annotation1 DETAILS
 *
 * @annotation2 DETAILS
 */
```
Where:
* `SHORT_DESC` is a short description of the class or method. Must be ended by a dot.
* `LONG_DESC` is a big paragraph that contains more details.
* `@annotation1` and `@annotation2` are simple PHPDoc annotations such as `@return` or `@param`.

Notice that each part of the doc block must be followed by an empty space. This helps in improving readability.