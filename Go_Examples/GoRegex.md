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

- [ ] Method: Match
  - [ ] Description: Test a string for matching a byte slice 
  - [ ] Signature: func Match(patter n string, b []byte) (matched bool, err error)

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
