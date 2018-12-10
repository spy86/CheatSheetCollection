When using strpos() ensure to do the comparison the right way.
Important: use the correct comparsion operator!
With strpos() functions always use the identical operator `"==="` or `"!=="` and compare to `"false"`
### CORRECT	
```php
if (strpos($str, $substr) === false) {
if (strpos($str, $substr) !== false) {
```
### WRONG	
```php
if (strpos($str, $substr) != false) {
if (strpos($str, $substr) == false) {
```
The reason for using the identical operators (that also check for the type of the value) `"==="` or `"!=="` is that `strpos(`) might return `"0"` for match at the beginning or `"false"` for no match which cannot be distinguished by `"=="` or `"!="`.
### Case Sensitivity
Simply use stripos() instead of strpos()
**strpos()**	case sensitive searching
**stripos()**	case insensitive searching

### Search From Offset
If you want to continue a search or want to skip something at the start use an offset as third parameter:
`if (strpos($str, $substr, 5) === false) {`
By using the return value of strpos() you can do repeated searches:
```php
$pos1 = strpos($str, $substr);
$pos2 = strpos($str, $substr, $pos1 + strlen($pos1));
```
### Search Backwards
There is an additional set of methods for backwards searching:
**strrpos()**	case sensitive backwards searching
**strripos()**	case insensitive backwards searching

### Extract Found Strings
If you want to extract a string at the position you've found you need to use the substr() method. An example:
```php
$pos = strpos($str, $substr);
$result = substr($str, $pos);
```

### When not to use strpos()?
Do not use `strpos()` if you want to do the following things:

- Test for a pattern at the start or end of a string -> use preg_match()
- Extract multiple substrings -> use preg_match()
- Match a string for a complex pattern -> use preg_match()
- If you want to split a string a delimiters -> use strpbrk()

### About Performance
If you are wondering how fast strpos() is compared to using regular expressions check this post: `strpos()` vs `preg_match()`
