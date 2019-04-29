First import the regexp package
```go
    import regexp
```
### Matching
```go
    match, _ := regexp.MatchString("[a-zA-Z0-9]+", input)
```
match will be true if the pattern matches. To return the first match as
string use
```go
    matchstr := regexp.FindString("([a-zA-Z0-9]+)", input)
```
To return all matches:
```go
    matches := regexp.FindAllString("([a-zA-Z0-9]+)", input)
```
### Matching Methods

There are different matching methods


| Method                | Description           | Signature             |
|-----------------------|-----------------------|-----------------------|
| Match                 |Test a string for matching a byte slice|func Match(pattern string, b []byte) (matched bool, err error)|
| MatchString| Test a string for match another string| func MatchString(pattern string, s string) (matched bool, err error)|
| Find\| Find first byte slices match and return it| func (re *Regexp) Find(b []byte) []byte|


### Replacing

To replace text use ReplaceAll or ReplaceAllString
```go
    func (re *Regexp) ReplaceAll(src, repl []byte) []byte
    func (re *Regexp) ReplaceAllString(src, repl string) string
```
e.g.
```go
    result := regexp.Compile("\s+").ReplaceAllString(input, " ")
```
to collapse all whitespaces

### Precompiled expressions

Create expression with
```go
    r, _ := regexp.Compile("[a-zA-Z0-9]+")
```
and use it in method form
```go
    r.MatchString(input)
```
