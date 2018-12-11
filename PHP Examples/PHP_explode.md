### Syntax
Use implode() in one of the following syntax variants with $delimiter being the separator string.
```php
$array = explode($delimiter, $string);
$array = explode($delimiter, $string, $limit);
```
Simple Examples
```php
$fields = explode(',', $csv);
$lines = implode('\n', $text);
```
### Advanced Usage
explode() is often used in conjuction with implode() to do something really useful.
```php
# Replace separator ';' with ','
$result = implode(',', explode(';', $input));
```