This post gives some simple examples for using regular expressions with preg_replace() in PHP scripts.
### Syntax
While full syntax is
```php
mixed preg_replace ( mixed $pattern , mixed 
$replacement , mixed $subject [, int $limit = -1 [, int &$count ]] )
```
### Simple Replacing
```php
$result = preg_replace('/abc/', 'def', $string);   # Replace all 'abc' with 'def'
$result = preg_replace('/abc/i', 'def', $string);  # Replace with case insensitive matching
$result = preg_replace('/\s+/', '', $string);      # Strip all whitespaces
```
### Advanced Usage
Multiple replacements:
```php
$result = preg_replace(
    array('/pattern1/', '/pattern2/'),
    array('replace1', 'replace2'),
    $string
);
```
Replacement Back References:
```php
$result = preg_replace('/abc(def)hij/', '/\\1/', $string);
$result = preg_replace('/abc(def)hij/', '/$1/', $string);
$result = preg_replace('/abc(def)hij/', '/${1}/', $string);
```
Do only a finite number of replacements:
```php
# Perform maximum of 5 replacements
$result = preg_replace('/abc/', 'def', $string, -1, 5);
```
Multi-line replacement
```php
# Strip HTML tag
$result = preg_replace('#<span id="15">.*</span>#m', '', $string);
```