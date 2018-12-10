### Syntax
Use implode() in one of the following syntax variants with $glue being the join string and $array an array of strings.
```php
$result = implode($glue, $array);
$result = implode($array);
```

Simple Examples
```php
$csv = implode(',', $fields);
$text = implode('\n', $lines);

# Debug output array keys
print "keys: ".implode(' ', array_keys($array));
```
### Advanced Usage
implode() is often used in conjuction with explode() to do something really useful.
```php
# Replace separator ';' with ','
$result = implode(',', explode(';', $input));
```