### Creating Arrays
Lists
```php
$a = array(1, 2, 3, 4);	
$b = array("abc", "def", "ghi");
$empty = array();
```
Assign values to specific indizes:

```php
$list = array();
$list[1] = 'Tom';
$list[45] = 'Sam';
$list[100] = 'Julie';
```

### Hashes
To create an associative array create a list of key/value pairs:
```php
$h = array(
	'command'	=> 'grep',
	'path'		=> '/usr/bin',
	'options'	=> '-ac',
	'param1'	=> '"pattern"',
	'param2'	=> '/data/file1.txt'
);
```
To create a multi-dimensional array just nest array() declarations as values:

### Nesting Arrays
```php
$a = array(
	array("key1", 4, 0, "description 1"),
	array("key2", 0, 33, ""),
	array("", 0, 10000, "something)
);
```
### Array <-> String
```php
$s = implode($a, ",");
$a = explode($s, ",");

array_push($a, "new value");
array_unshift($a, "new value");

$value = array_pop($a);
$value = array_shift($a);
```

### Array Functions

```php
array_walk($a, 'callback_function');

$a = array_unique($a);

$keys    = array_keys($a);
$indices = array_keys($a, 'key value');
```

Get Length

```php
echo count($list);
```

List for

```php
for($i = 0; $i < count($list); $i++) {
	echo "$i: $list[$i]\n";
}
```

### Iterating Arrays

List foreach
```php
foreach($list as $element) {
	print "$element\n";
}
```

Hash foreach
```php
foreach($hash as $key => $value) {
	print "$key => $value\n";
}
```