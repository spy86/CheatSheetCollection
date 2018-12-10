Use strrpos() to do backwards matching for substrings in PHP. When using strrpos() ensure to do the comparison the right way.
### Important: Use Correct Comparsion Operator!
Only ever compare with the identical operators `"==="` , `"!=="` and only ever compare with false

### Postive match
```php
if (strrpos($str, $substr) !== false) {
     echo("Does match!")
}
```
### Negative match
```php
if (strrpos($str, $substr) === false) {
     echo("Does not match.")
}
```

### Check out for more details
Search From Offset
If you want to continue a search or want to skip something at the end use an offset as third parameter:
`if (strrpos($str, $substr, 5) === false) {`
By using the return value of strrpos() you can do repeated searches:
```php
$pos1 = strrpos($str, $substr);
$pos2 = strrpos($str, $substr, $pos1 + strlen($pos1));
```