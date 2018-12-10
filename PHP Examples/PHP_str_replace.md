### Syntax
`$result = str_replace ($pattern, $replacement, $string);`
For case-insensitive replacement:
`$result = str_ireplace ($pattern, $replacement, $string);`
### Multiple Replacements
If you have a list of replacements you can perform it like this
```python
$pattern      = array('ä', 'ü', 'ö');
$replacements = array('&auml;', '&uuml;', '&ouml;');

$result = str_replace($pattern, $replacements, $string);
```
### Count Replacements
To get the number of substitutions pass a 4th call by reference parameter:
`$result = str_replace($pattern, $replacement, $string, $count);`
### Alternative Methods
As `str_replace` doesn't suit all use cases you sometimes have to switch to other PHP methods:

- Matching with regex: see
- Limit to n substitutions:
- "+""
- strpos + substr_replace