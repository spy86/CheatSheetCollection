First import the regexp package

    import regexp

### Matching

    match, _ := regexp.MatchString("[a-zA-Z0-9]+", input)

match will be true if the pattern matches. To return the first match as
string use

    matchstr := regexp.FindString("([a-zA-Z0-9]+)", input)

To return all matches:

    matches := regexp.FindAllString("([a-zA-Z0-9]+)", input)

### Matching Methods

There are different matching methods


| Method                | Description           | Signature             |
|-----------------------|-----------------------|-----------------------|
| Match                 | Test a string for     |     func Match(patter |
|                       | matching a byte slice | n string, b []byte) ( |
|                       |                       | matched bool, err err |
|                       |                       | or)                   |
|                       |                       |                       |
| MatchString           | Test a string for     |     func MatchString( |
|                       | match another string  | pattern string, s str |
|                       |                       | ing) (matched bool, e |
|                       |                       | rr error)             |
|                       |                       |                       |
| Find\                 | Find first byte       |     func (re *Regexp) |
| FindIndex\            | slices match and      |  Find(b []byte) []byt |
| FindSubmatch\         | return it             | e                     |
| FindSubmatchIndex     |                       |     func (re *Regexp) |
|                       |                       |  FindIndex(b []byte)  |
|                       |                       | (loc []int)           |
|                       |                       |     func (re *Regexp) |
|                       |                       |  FindSubmatch(b []byt |
|                       |                       | e) [][]byte           |
|                       |                       |     func (re *Regexp) |
|                       |                       |  FindSubmatchIndex(b  |
|                       |                       | []byte) []int         |
|                       |                       |                       |
| FindString\           | Find first string     |     func (re *Regexp) |
| FindStringIndex\      | match and return it   |  FindString(s string) |
| FindStringSubmatch\   |                       |  string               |
| FindStringSubmatchInd |                       |     func (re *Regexp) |
| ex                    |                       |  FindStringIndex(s st |
|                       |                       | ring) (loc []int)     |
|                       |                       |     func (re *Regexp) |
|                       |                       |  FindStringSubmatch(s |
|                       |                       |  string) []string     |
|                       |                       |     func (re *Regexp) |
|                       |                       |  FindStringSubmatchIn |
|                       |                       | dex(s string) []int   |
|                       |                       |                       |
| FindAll\              | Like the              | Like the              |
| FindAllIndex\         | Find/FindString       | Find/FindString       |
| FindAllString\        | methods, just         | methods, just         |
| FindAllStringIndex\   | returning all matches | returning arrays of   |
| FindAllStringSubmatch |                       | matches               |
| \                     |                       |                       |
| FindAllStringSubmatch |                       |                       |
| Index\                |                       |                       |
|                       |                       |                       |

### Replacing

To replace text use ReplaceAll or ReplaceAllString

    func (re *Regexp) ReplaceAll(src, repl []byte) []byte
    func (re *Regexp) ReplaceAllString(src, repl string) string

e.g.

    result := regexp.Compile("\s+").ReplaceAllString(input, " ")

to collapse all whitespaces

### Precompiled expressions

Create expression with

    r, _ := regexp.Compile("[a-zA-Z0-9]+")

and use it in method form

    r.MatchString(input)
