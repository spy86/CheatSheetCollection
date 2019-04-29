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
***
- [ ] Method: MatchString
  - [ ] Description: Test a string for match another string
  - [ ] Signature: func MatchString(pattern string, s string) (matched bool, err error)
***
- [ ] Method: Find
  - [ ] Description: Find first byte slices match and return it
  - [ ] Signature: func (re *Regexp) Find(b []byte) []bye
***
- [ ] Method: FindIndex
  - [ ] Description: Find first byte slices match and return it
  - [ ] Signature: func (re *Regexp) FindIndex(b []byte) (loc []int)
***
- [ ] Method: FindSubmatch
  - [ ] Description: Find first byte slices match and return it
  - [ ] Signature: func (re *Regexp) FindSubmatch(b []byte) [][]byte
***
- [ ] Method: FindSubmatchIndex
  - [ ] Description: Find first byte slices match and return it
  - [ ] Signature: func (re *Regexp) FindSubmatchIndex(b[]byte) []int)
***
- [ ] Method: FindString
  - [ ] Description: Find first string match and return it
  - [ ] Signature: func (re *Regexp) FindString(s string) string
***
- [ ] Method: FindStringIndex
  - [ ] Description: Find first string match and return it
  - [ ] Signature: func (re *Regexp) FindStringIndex(s string) (loc []int)
***
- [ ] Method: FindStringSubmatch
  - [ ] Description: Find first string match and return it
  - [ ] Signature: func (re *Regexp) FindStringSubmatch(s string) []string
***
- [ ] Method: FindStringSubmatchIndex
  - [ ] Description: Find first string match and return it
  - [ ] Signature: func (re *Regexp FindStringSubmatchIn dex(s string) []int
***
- [ ] Method: FindAll
  - [ ] Description: Like the Find/FindString methods, just returning all matches
  - [ ] Signature: Like the Find/FindString methods, just returning arrays of matches
***
- [ ] Method: FindAllIndex
  - [ ] Description: Like the Find/FindString methods, just returning all matches
  - [ ] Signature: Like the Find/FindString methods, just returning arrays of matches
***
- [ ] Method: FindAllString
  - [ ] Description: Like the Find/FindString methods, just returning all matches   
  - [ ] Signature: Like the Find/FindString methods, just returning arrays of matches
***
- [ ] Method: FindAllStringIndex
  - [ ] Description: Like the Find/FindString methods, just returning all matches
  - [ ] Signature: Like the Find/FindString methods, just returning arrays of matches
***
- [ ] Method: FindAllStringSubmatch
  - [ ] Description: Like the Find/FindString methods, just returning all matches
  - [ ] Signature: Like the Find/FindString methods, just returning arrays of matches
***
- [ ] Method: FindAllStringSubmatch Index
  - [ ] Description: Like the Find/FindString methods, just returning all matches
  - [ ] Signature: Like the Find/FindString methods, just returning arrays of matches
  
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
