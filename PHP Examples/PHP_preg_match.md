Use preg_match() to match strings with regular expressions. Check the return value for true to see if the expression did match.
### Syntax of preg_match
While full syntax is
```php
int preg_match ( string $pattern , string $subject 
     [, array &$matches [, int $flags = 0 [, int $offset = 0 ]]] )
```
You propably will use `preg_match()` mostly with two parameters for simply matching checks or with three to extract matches. You probably won't use the 4th and 5th parameter which can be used to return match offsets and limit matching to a given offset in the string.
### Simple String Checks
Here are some syntax examples that check strings for certain content: **Basic matching**
```php
preg_match("/PHP/", "PHP")       # Match for an unbound literal
preg_match("/^PHP/", "PHP")      # Match literal at start of string
preg_match("/PHP$/", "PHP")      # Match literal at end of string
preg_match("/^PHP$/", "PHP")     # Match for exact string content
preg_match("/^$/", "")           # Match empty string
```

**Using different regex delimiters**
```php
preg_match("/PHP/", "PHP")                # / as commonly used delimiter
preg_match("@PHP@", "PHP")                # @ as delimiter
preg_match("!PHP!", "PHP")                # ! as delimiter
```

**Changing the delimiter becomes useful in some cases**
```php
preg_match("/http:\/\//", "http://");     # match http:// protocol prefix with / delimiter
preg_match("#http://#",   "http://")      # match http:// protocol prefix with # delimiter
```

**Case sensitivity**
```php
preg_match("/PHP/", "PHP")                # case sensitive string matching
preg_match("/php/i", "PHP")               # case in-sensitive string matching
```

**Matching with wildcards**
```
preg_match("/P.P/",     "PHP")            # match a single character
preg_match("/P.*P/",    "PHP")            # match multipe characters
preg_match("/P[A-Z]P/", "PHP")            # match from character range A-Z
preg_match("/[PH]*/",   "PHP")            # match from character set P and H
preg_match("/P\wP/",    "PHP")            # match one word character
preg_match("/\bPHP\b/", "regex in PHP")   # match the word "PHP", but not "PHP" as larger string
```

**Using quantifiers**
```php
preg_match("/[PH]{3}/",   "PHP")          # match exactly 3 characters from set [PH]
preg_match("/[PH]{3,3}/", "PHP")          # match exactly 3 characters from set [PH]
preg_match("/[PH]{,3}/",  "PHP")          # match at most 3 characters from set [PH]
preg_match("/[PH]{3,}/",  "PHP")          # match at least 3 characters from set [PH]
```
### Extracting Data
To extract data using regular expression we have to use capture/grouping syntax.
Some basic examples
```php
# Extract everything after the literal "START"
preg_match("/START(.*)/", $string, $results)   

# Extract the number from a date string 
preg_match("/(\d{4})-(\d{2})-(\d{2})/", "2012-10-20", $results)

# Nesting of capture groups, extract full name, and both parts...
preg_match("/name is ((\w+), (\w+))/", "name is Doe, John", $results)
```
So you basically just enclose the sub patterns you want to extract with braces and fetch the results by passing a third parameter which preg_match() will fill as an array.
Named Capture Groups
```php
# Extract the number from a date string 
preg_match("/(?P<year>\d{4})-(?P<month>\d{2})-(?P<day>\d{2})/", "2012-10-20", $results)
```
Now the $result array will additionally to the position matches 1, 2 and 3 contain the keys "year", "month" and "day". The advantage is never having to think of the capture positions anymore when you modify the expression!

### Check Processing Errors!
While it might often be unimportant be aware that applying a regular expression might fail due to PCRE constraints. This usually happens when matching overly long strings or strings with faulty encoding. The only way to notice that preg_match() was not able to check the string is by calling
`preg_last_error()`
Only if it returns PREG_NO_ERROR you got a safe result! Consider this when using preg_match() for security purposes.

### Suggested Reading
 - [PHP Pocket Reference: PHP in your pocket](https://www.amazon.de/PHP-Pocket-Reference-your-pocket/dp/1491969091/ref=as_li_ss_il?s=books-intl-de&ie=UTF8&qid=1509402246&sr=1-5&keywords=php+regular+expressions&linkCode=li3&tag=lzone04-21&linkId=b19a6d2b9e501a2db36770b028ed72dc)
 - [Regular Expression Pocket Reference: Regular Expressions for Perl, Ruby, PHP, Python, C, Java and .NET (Pocket Reference (O'Reilly))](https://www.amazon.de/Regular-Expression-Pocket-Reference-Expressions/dp/0596514271/ref=as_li_ss_il?s=books-intl-de&ie=UTF8&qid=1509402246&sr=1-1&keywords=php+regular+expressions&linkCode=li3&tag=lzone04-21&linkId=ef88a1018bc76512ceded94172f603e0)
 