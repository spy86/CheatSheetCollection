### Syntax
`$result = date(<format>);`
### Format Examples
```php
date("c")			# ISO 8601 date "2015-12-01T16:00+00:00
date("r")			# RFC 2822 date "Thu, 29 Jan 2099 10:11:00 +0100"
date("U")			# Unix timestamp
date('l jS \of F Y h:i:s A')	# Friday 13th of March 2015 08:35:01 PM
date("Y-m-d H:i:s")		# 2015-03-13 08:35:01
date("m/d/y");			# 05/02/2015
date("H:M:S");			# 20:01:59
```
### Since PHP 5.2 there are predefined constants you can use:
```php
date(DATE_ISO8601)		# "2015-03-13T20:38:00+0100"
date(DATE_RFC2822)		# "Fri, 13 Mar 2015 20:41:22 +0100"
date(DATE_RFC822)		# "Fri, 13 Mar 15 20:41:41 +0100"
date(DATE_RFC850)		# "Friday, 13-Mar-15 20:38:00"
date(DATE_COOKIE)		# "Friday, 13-Mar-15 20:38:00 CET"
```
### Format Codes
Citation from the PHP [documentation:](http://php.net/manual/en/function.date.php)